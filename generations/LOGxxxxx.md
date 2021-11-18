---
erp.entity: Logistics.Inventory.StoreOrders
erp.type: generation
---

# LOGxxxxx Create Store Transaction for fulfilled ..

## Basic Information

| Module                          | Logistics.Inventory                                               |
| :------------------------------ | ----------------------------------------------------------------- |
| Code                            | LOGxxxxx                                                               |
| Parent Document                 | StoreOrder                                                        |
| Sub-document                    | StoreTransaction                                                  |
| Full Name                       | Create Store transactions (with waiting for warehouse operations) |
| Status                          | [ACTIVE](xref:generation-procedures) |
| Deterministic                   | [YES](xref:document-generation-and-transitional-documents) |
| Supports Transitional Documents | [NO](xref:document-generation-and-transitional-documents) |
| Replaces                        | -                                                                 |
| Orphan Rows                     | Ignore                                                            |
| Introduced In Version           | 2018.2                                                            |
| Date of Suspension              | -                                                                 |

## Business Logic

This generation creates Store Transaction based on the fulfillment of the Store Order, regardless of which module executed the order. 
It is often used when the Store Order is executed by another module (eg WMS) or an external application.
 

The Store Transaction’s header is created based on the Store Order’s header as follows:

```
Transaction.ParentStoreOrder = StoreOrder

Transaction.Store = StoreOrder.Store

Transaction.MovementType = StoreOrder.MovementType

Transaction.DocumentCurrency = StoreOrder.DocumentCurrency
```

> [!Note] 
> The attributes which are not specified here are filled in as described in [Standard Document Attributes](../reference/standard-document-attributes.md)

> [!Note] 
> The new store transaction is saved then and only when there is at least one line in it.

## Fulfillments

| Name                        | StoreOrderLineToStoreTransactionLine                         |
| :-------------------------- | ------------------------------------------------------------ |
| Parent Entity               | StoreOrderLine                                               |
| Child Entity                | StoreTransactionLine                                         |
| Parent / Child Relationship | StoreTransactionLine.ParentDocument = StoreOrder;StoreTransactionLine.ParentLineNo = StoreOrderLine.LineNo |

## [Metrics](../reference/metrics.md)

| Fulfillment Name                     |      Metric Name      |              Measurement Unit              | Parent Value                        | Child Value                               | New Record                                                   |
| :----------------------------------- | :-------------------: | :----------------------------------------: | :---------------------------------- | :---------------------------------------- | :----------------------------------------------------------- |
| StoreOrderLineToStoreTransactionLine | MStandardQuantityBase | StoreOrderLine.Product.BaseMeasurementUnit | StoreOrderLine.StandardQuantityBase | StoreTransactionLine.StandardQuantityBase | YES                                                          |
| StoreOrderLineToStoreTransactionLine |       MQuantity       |        StoreOrderLine.QuantityUnit         | StoreOrderLine.Quantity             | StoreTransactionLine.Quantity             | NO                                                           |
| StoreOrderLineToStoreTransactionLine |     MQuantityBase     | StoreOrderLine.Product.BaseMeasurementUnit | StoreOrderLine.QuantityBase         | StoreTransactionLine.QuantityBase         | NO                                                           |
| StoreOrderLineToStoreTransactionLine |       MLineCost       |        StoreOrder.DocumentCurrency         | StoreOrderLine.LineCost             | StoreTransactionLine.LineCost             | if (StoreOrder.MovementType== Receipt) {New Record = YES},else {New Record = NO} |

The lines of the new document are created based on the data for the Fulfilled Part of quantities by Store Transactions that are already created (for more information, see topic [Discrepancy System](../reference/discrepancy-system.md)). The new StoreTransactionLine is created as follows:

```
StoreTransactionLine.LineNo = StoreOrderLine.LineNo

StoreTransactionLine.ParentStoreOrderLine = StoreOrderLine

StoreTransactionLine.StoreBin = IFF (StoreOrderLine.StoreBin != NULL, StoreOrderLine.StoreBin, IFF(ProductDefaultStoreBin(Product == StoreTransactionLine.Product && Store = StoreOrder.Store).Count() == 1, ProductDefaultStoreBin.DefaultBin, StoreOrder.Store.DefaultStoreBin))

StoreTransactionLine.OriginalProduct = StoreOrderLine.Product

StoreTransactionLine.Product = StoreOrderLine.Product

StoreTransactionLine.Lot = StoreOrderLine.Lot

StoreTransactionLine.SerialNumber = StoreOrderLine.SerialNumber

StoreTransactionLine.Quantity = StoreOrderLine.REMAINING(MQuantity)

StoreTransactionLine.QuantityUnit = StoreOrderLine.QuantityUnit

StoreTransactionLine.QuantityBase = StoreOrderLine.REMAINING(MQuantityBase)

StoreTransactionLine.StandardQuantityBase = StoreOrderLine.REMAINING(MStandardQuantityBase)

StoreTransactionLine.Notes = StoreOrderLine.Notes

StoreTransactionLine.UnitCost = StoreOrderLine.UnitCost

StoreTransactionLine.LineCost = if (StoreOrder.MovementType == Receipt) {StoreTransactionLine.LineCost = StoreOrderLine.REMAINING(MLineCost)}, else {StoreTransactionLine.LineCost = 0.00}

StoreTransactionLine.GuaranteePeriodDays = StoreOrderLine.GuaranteePeriodDays

StoreTransactionLine.ParentLineId = StoreOrderLine.ParentLineId

StoreTransactionLine.ProductVariant = StoreOrderLine.ProductVariant

StoreTransactionLine.ParentLineNo = StoreOrderLine.LineNo

StoreTransactionLine.TransactionTimestamp = StoreOrderLine.TransactionTimestamp
```
