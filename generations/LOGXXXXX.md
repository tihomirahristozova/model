---
erp.entity: 
erp.type: generation
---

# LOGXXXXX Create Warehouse Orders for Composite Products

## Basic Information

| Module                          | Logistics.WMS                                                |
| :------------------------------ | ------------------------------------------------------------ |
| Code                            | LOGXXXXX                                                      |
| Parent Document                 | Warehouse Requisition                                        |
| Sub-document                    | Warehouse Order                                              |
| Full Name                       | Create Simple Warehouse Orders (with saparate lines for the composite product components) |
| Status                          | [NEW](xref:generation-procedures) |
| Deterministic                   | [YES](xref:document-generation-and-transitional-documents) |
| Supports Transitional Documents | [NO](xref:document-generation-and-transitional-documents) |
| Supports Single Execution       | YES                                                          |
| Replaces                        | -                                                            |
| Orphan Rows                     | Ignore                                                       |
| Split Function                  | -                                                            |
| Version                         | Introduced: 2023 Updated: -                                 |
| Date of Suspension              | -                                                            |

## Business Logic

This generation is used to create Warehouse Orders from Warehouse Requisitions when the company is using Composite Products. Thе generation creates warehouse orders for both the noncomposite products and the composite products. What is special about this generation is that it creates two kinds of lines for the execution of the composite products. One line for the composite product and one line for each of its components.


**The Warehouse Order’s header is created based on the Warehouse Requisition’s header as follows:**
```
WarehouseOrder.DocumentDate = WarehouseRequisition.DocumentDate

WarehouseOrder.Warehouse = WarehouseRequisition.Warehouse

WarehouseOrder.WarehouseWorker = NULL
```

> [!Note]
> The attributes which are not specified here are filled in as described in [Standard Document Attributes](../reference/standard-document-attributes.md)

> [!Note]
> The new Warehouse Order is saved then and only when there is at least one line in it.

## Fulfillments

| Fulfilment Name                              | CompositeProductToWarehouseOrderLine                               |
| :------------------------------------------- | ------------------------------------------------------------ |
| Fulfilment Tracking Type                     | Fulfilment Table                                             |
| Parent Entity                                | WarehouseRequisitionLine |
| Fulfilment Table                             | DocumentFulfillment(where 'DocumentLineId == WarehouseRequisitionLineId')|
| Parent Entity/ Fulfilment Table Relationship | WarehouseRequisitionLine.Product = DocumentFulfillment.Product |

## [Metrics](../reference/metrics.md)

| Fulfilment Name                              |  Metric Name  |                   Measurement Unit                   | Parent Value                              | Fulfilment Table Value           | New Record |
| :------------------------------------------- | :-----------: | :--------------------------------------------------: | :---------------------------------------- | :------------------------------- | :--------- |
| CompositeProductToWarehouseOrderLine | MQuantityBase | WarehouseRequisitionLine.Product.BaseMeasurementUnit | WarehouseRequisitionLineLine.QuantityBase | DocumentFulfillment.QuantityBase | NO |
| CompositeProductToWarehouseOrderLine | MStandardQuantity | WarehouseRequisitionLine.Product.BaseMeasurementUnit | WarehouseRequisitionLineLine.StandardQuantity | DocumentFulfillment.StandardQuantity | YES |

**The Warehouse Order Lines creation**
<br/><br/>
The lines of the new document are created based on the data of the Planned records in the Document Fulfillments table. 
The table contains the information for the Fulfilled Part of quantities by the Warehouse Oders which have already been created.

> [!Note]
> Note that for the calculation of the Fulfilled Part are taken into account only the recods whoose Fulfillment Type is Planned.

<br/>

The creation starts with determining the kind of the product (composite or not) and the direction of movement.

Is the product a composite product?
A product is considered as composite when it has atleast one valid component. 
Valid composite product components are those for which:
- FromDate == null OR <= WarehouseOrder.DocumentDate
- ToDate == null OR >= WarehouseOrder.DocumentDate
- IsActive == true

What is the direction on the movement?
It depends on the parent requisition's Requisition Type which can be "Inbound" or "Outbound".

Depending on the answers on both questions system may create three types of warehouse order lines:
- a line executing a non-composite product;
- a line executing a composite product;
- a line/s executing the composite product's components.

**Non-composite products** 

If the parent requsition line's products is non-composite, the system will create a "traditional" warehouse order line with Receive or Dispatch task type.

**Warehouse Order Lines executing a non-composite product is created as follows**

```
WarehouseOrderLine.TaskType = If (WarehouseRequisition.RequisitionType = Inbound )

                            , then WarehouseOrderLine.TaskType = Receive

                            , else WarehouseOrderLine.TaskType = Dispatch

WarehouseOrderLine.Product = WarehouseRequisitionLine.Product

WarehouseOrderLine.Lot = WarehouseRequisitionLine.Lot

WarehouseOrderLine.SerialNumber = WarehouseRequisitionLine.SerialNumber

WarehouseOrderLine.ProductVariant = WarehouseRequisitionLine.ProductVariant

WarehouseOrderLine.QuantityUnit = WarehouseRequisitionLine.QuantityUnit

WarehouseOrderLine.Quantity =  CONVERT(WarehouseOrderLine.StandardQuantity, WarehouseOrderLine.QuantityUnit)

WarehouseOrderLine.QuantityBase = WarehouseRequisitionLine.REMAINING(MQuantityBase)

WarehouseOrderLine.StandardQuantity = WarehouseRequisitionLine.REMAINING(MStandardQuantity)

WarehouseOrderLine.LogisticUnit = NULL

WarehouseOrderLine.WarehouseZone = NULL

WarehouseOrderLine.WarehouseLocation =NULL

WarehouseOrderLine.ToWarehouseLocation = NULL

WarehouseOrderLine.WarehouseWorker = NULL

WarehouseOrderLine.Notes = WarehouseRequisitionLine.Notes

WarehouseOrderLine.ParentDocument = WarehouseRequisition

WarehouseOrderLine.ParentLineNo = WarehouseRequisitionLine.LineNo
```


**Composite products** 

If the parent requsition line contains a composite product are created two sets of Warehouse Order Lines - one for the composite product and one for each of its components.

**The Warehouse Order Lines executing the composite product are created as follows**
```
WarehouseOrderLine.TaskType = If (WarehouseRequisition.RequisitionType = Inbound )

                            , then WarehouseOrderLine.TaskType = Dekit

                            , else WarehouseOrderLine.TaskType = Kit

WarehouseOrderLine.Product = WarehouseRequisitionLine.Product

WarehouseOrderLine.Lot = WarehouseRequisitionLine.Lot

WarehouseOrderLine.SerialNumber = WarehouseRequisitionLine.SerialNumber

WarehouseOrderLine.ProductVariant = WarehouseRequisitionLine.ProductVariant

WarehouseOrderLine.QuantityUnit = WarehouseRequisitionLine.QuantityUnit

WarehouseOrderLine.Quantity =  CONVERT(WarehouseOrderLine.StandardQuantity, WarehouseOrderLine.QuantityUnit)

WarehouseOrderLine.QuantityBase = WarehouseRequisitionLine.REMAINING(MQuantityBase)

WarehouseOrderLine.StandardQuantity = WarehouseRequisitionLine.REMAINING(MStandardQuantity)

WarehouseOrderLine.LogisticUnit = NULL

WarehouseOrderLine.WarehouseZone = NULL

WarehouseOrderLine.WarehouseLocation =NULL

WarehouseOrderLine.ToWarehouseLocation = NULL

WarehouseOrderLine.WarehouseWorker = NULL

WarehouseOrderLine.Notes = WarehouseRequisitionLine.Notes

WarehouseOrderLine.ParentDocument = WarehouseRequisition

WarehouseOrderLine.ParentLineNo = WarehouseRequisitionLine.LineNo
```


<br/>
**The Warehouse Order Lines executing the composite product's components are created as follows**

First we are getting all Composite Product Components where Composite Product is equal to the Product of the Warehouse Requisition Line. Then we are filtering only the valid componets.
Valid components are those for which:
- FromDate == null OR <= WarehouseOrder.DocumentDate
- ToDate == null OR >= WarehouseOrder.DocumentDate
- IsActive == true

Then we are creating new Warehouse Order Line for each of the valid components:
```
WarehouseOrderLine.TaskType = If (WarehouseRequisition.RequisitionType = Inbound )

                            , then WarehouseOrderLine.TaskType = ComponentReceive

                            , else WarehouseOrderLine.TaskType = ComponentDispatch

WarehouseOrderLine.Product = CompositeProductComponent.ComponentProductId	

WarehouseOrderLine.Lot = NULL

WarehouseOrderLine.SerialNumber = NULL

WarehouseOrderLine.ProductVariant = NULL

WarehouseOrderLine.QuantityUnit = FIRST(MeasurementUnits where SystemUnit = Pieces)

WarehouseOrderLine.Quantity = WarehouseRequisitionLine.StandardQuantity * Component.Quantity

WarehouseOrderLine.QuantityBase = WarehouseRequisitionLine.StandardQuantity * Component.Quantity

WarehouseOrderLine.StandardQuantity = WarehouseRequisitionLine.StandardQuantity * Component.Quantity

WarehouseOrderLine.LogisticUnit = NULL

WarehouseOrderLine.WarehouseZone = NULL

WarehouseOrderLine.WarehouseLocation = NULL

WarehouseOrderLine.ToWarehouseLocation = NULL

WarehouseOrderLine.WarehouseWorker = NULL

WarehouseOrderLine.Notes = WarehouseRequisitionLine.Notes

WarehouseOrderLine.ParentDocument = WarehouseRequisition

WarehouseOrderLine.ParentLineNo = WarehouseRequisitionLine.LineNo
```

Once all of the Warehouse Order Lines are created and before the document is saved, the generation generates records in the Document Fulfillment table.
These records reflect the quantities fulfilled by the current iteration of the generation procedure and are needed to determine the quantities for subsequent generation iterations.

**The new Document Fulfillment is created as follows:**
**Important: Note that document fulfillments are NOT created for the warehouse order lines which are executing the product's components. **
```
DocumentFulfillment.Document = WarehouseRequisition

DocumentFulfillment.DocumentLineId = WarehouseRequisitionLineId

DocumentFulfillment.LineNo = WarehouseRequisitionLine.LineNo

DocumentFulfillment.FulfillmentType = Planned

DocumentFulfillment.IsFinal = If (WarehouseOrder.DocumentType.GenerateSingleDocument = true)

                          , then DocumentFulfillment.IsFinal = true

                          , else DocumentFulfillment.IsFinal = false

DocumentFulfillment.LineType = Line

DocumentFulfillment.QuantityBase = WarehouseOrderLine.QuantityBase

DocumentFulfillment.StandardQuantity = WarehouseOrderLine.StandardQuantity

DocumentFulfillment.Product = WarehouseOrderLine.Product

DocumentFulfillment.Lot = WarehouseOrderLine.Lot

DocumentFulfillment.SerialNumber = WarehouseOrderLine.SerialNumber

DocumentFulfillment.ProductVariant = WarehouseOrderLine.ProductVariant

DocumentFulfillment.DestinationEntityName = Wms_Warehouse_Order_Lines
```
