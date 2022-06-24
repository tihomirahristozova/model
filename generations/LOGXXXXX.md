---
erp.entity: Logistics.Wms.WarehouseRequisitions_
erp.type: generation
---

# LOGXXXXX Create Warehouse Orders for Composite Products

## Basic Information

| Module                          | Logistics.WMS                                                |
| :------------------------------ | ------------------------------------------------------------ |
| Code                            | LOGXXXXX                                                      |
| Parent Document                 | Warehouse Requisition                                        |
| Sub-document                    | Warehouse Order                                              |
| Full Name                       | Create Warehouse Orders for Composite Products               |
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

This generation is used to create Warehouse Orders from Warehouse Requisitions for the Composite Products. Thе generation takes the Warehouse Order Lines with Composite Products and
splits them into several Warehouse Order Lines - one for each of the Composite Product's Components.

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

| Fulfilment Name                              | CompositeProductComponentsToWarehouseOrderLine                               |
| :------------------------------------------- | ------------------------------------------------------------ |
| Fulfilment Tracking Type                     | Fulfilment Table                                             |
| Parent Entity                                | CompositeProductsComponents(where 'CompositeProduct == WarehouseRequisitionLine.Product' AND 'FromDate == null OR <= WarehouseOrder.DocumentDate' AND 'ToDate == null OR >= WarehouseOrder.DocumentDate') |
| Fulfilment Table                             | DocumentFulfillment(where'DocumentLineId == WarehouseRequisitionLineId')|
| Parent Entity/ Fulfilment Table Relationship | CompositeProductsComponent.ComponentProductId = DocumentFulfillment.ProductId |


| Fulfilment Name                              | CompositeProductToWarehouseOrderLine                               |
| :------------------------------------------- | ------------------------------------------------------------ |
| Fulfilment Tracking Type                     | Fulfilment Table                                             |
| Parent Entity                                | WarehouseRequisitionLine |
| Fulfilment Table                             | DocumentFulfillment(where 'DocumentLineId == WarehouseRequisitionLineId')|
| Parent Entity/ Fulfilment Table Relationship | WarehouseRequisitionLine.Product = DocumentFulfillment.Product |

## [Metrics](../reference/metrics.md)

| Fulfilment Name                              |  Metric Name  |                   Measurement Unit                   | Parent Value                              | Fulfilment Table Value           | New Record |
| :------------------------------------------- | :-----------: | :--------------------------------------------------: | :---------------------------------------- | :------------------------------- | :--------- |
| CompositeProductComponentsToWarehouseOrderLine | MQuantityBase | PCS | WarehouseRequisitionLineLine.QuantityBase * CompositeProductsComponent.Quantity | DocumentFulfillment.QuantityBase | NO |
| CompositeProductComponentsToWarehouseOrderLine | MStandardQuantity | PCS | WarehouseRequisitionLineLine.StandardQuantity * CompositeProductsComponent.Quantity| DocumentFulfillment.StandardQuantity | YES |
| CompositeProductToWarehouseOrderLine | MQuantityBase | WarehouseRequisitionLine.Product.BaseMeasurementUnit | WarehouseRequisitionLineLine.QuantityBase | DocumentFulfillment.QuantityBase | NO |
| CompositeProductToWarehouseOrderLine | MStandardQuantity | WarehouseRequisitionLine.Product.BaseMeasurementUnit | WarehouseRequisitionLineLine.StandardQuantity | DocumentFulfillment.StandardQuantity | YES |

<br/><br/>
The lines of the new document are created based on the data of the Planned records in the Document Fulfillments table. 
The table contains the information for the Fulfilled Part of quantities by the Warehouse Oders which have already been created.

> [!Note]
> Note that for the calculation of the Fulfilled Part are taken into account only the recods whoose Fulfillment Type is Planned.

<br/>

**For each Warehouse Requisition Line are created two sets of Warehouse Order Lines - one for each of the components and one for the composite productin the following way:**
<br/>
**The Warehouse Order Lines which are executing the Components**

First we are getting all Composite Product Components where Composite Product is equal to the Product of the Warehouse Requisition Line. Then we are filtering only the valid componets.
Valid components are those for which:
- FromDate == null OR <= WarehouseOrder.DocumentDate
- ToDate == null OR >= WarehouseOrder.DocumentDate
**- IsActive ???????**

Then we are creating new Warehouse Order Line for each of the valid components:
```
WarehouseOrderLine.TaskType = If (WarehouseRequisition.RequisitionType = Inbound )

                            , then WarehouseOrderLine.TaskType = ComponentReceive

                            , else WarehouseOrderLine.TaskType = ComponentDispatch

WarehouseOrderLine.Product = CompositeProductComponent.ComponentProductId	

WarehouseOrderLine.Lot = NULL

WarehouseOrderLine.SerialNumber = NULL

WarehouseOrderLine.ProductVariant = NULL

WarehouseOrderLine.QuantityUnit = **PCS ?????????????????????????????????**

WarehouseOrderLine.Quantity = CONVERT(WarehouseOrderLine.StandardQuantity, WarehouseOrderLine.QuantityUnit)

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

**The Warehouse Order Lines which are executing the CompositeProduct**

After the creation of the lines for the Components, we have to create a line for the Composite Product as well:
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


Once all of the Warehouse Order Lines are created and before the document is saved, the generation generates records in the Document Fulfillment table.
These records reflect the quantities fulfilled by the current iteration of the generation procedure and are needed to determine the quantities for subsequent generation iterations.

**The new Document Fulfillment is created as follows:**

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
