# Metrics

## Details

Sometimes, when creating a new child/sub document by a generation procedure, some of the values of the child fields are not just copied from the parent document but need to be calculated. **The Metrics** are used when the calculation is based on the data about the unfulfilled quantities and amounts by the child documents that have already been created. It usually applies when the parent value has to be fully exhausted by its child values. **Metrics** bring the information which values have to be compared, how and whether the remaining result (if different from zero) has to lead to the creation of a new document or not. Each comparison is a separate metric.



## Example:

> **If we have the information about two metrics with the following description:**
>
> | Fulfillment Name                     | Metric Name           | Measurement Unit                           | Parent Value                        | Child Value                          | New Record |
> | :----------------------------------- | :-------------------- | :----------------------------------------- | :---------------------------------- | :----------------------------------- | :--------- |
> | StoreOrderLineToStoreTransactionLine | MStandardQuantityBase | StoreOrderLine.Product.BaseMeasurementUnit | StoreOrderLine.StandardQuantityBase | TransactionLine.StandardQuantityBase | YES        |
> | StoreOrderLineToStoreTransactionLine | MQuantityBase         | StoreOrderLine.Product.BaseMeasurementUnit | StoreOrderLine.QuantityBase         | TransactionLine.QuantityBase         | NO         |
>
> **And we know that:**
>
> TransactionLine.StandardQuantityBase = StoreOrderLine.REMAINING(StandardQuantityBase)
>
> TransactionLine.QuantityBase = StoreOrderLine.REMAINING(QuantityBase)
>
> , where:
>
> -  *"TransactionLine.StandardQuantityBase"* and *"TransactionLine.QuantityBase"* are the ordered by the parent line quantity values;
> - *"StoreOrderLine.REMAINING(StandardQuantityBase)"* and *"StoreOrderLine.REMAINING(QuantityBase)"* are the ordered quantities which are not yet fullfilled by subdocumets i.e. (**TransactionLine.StandardQuantityBase - SUM(Child.StoreOrderLine.StandardQuantityBase) and (TransactionLine.QuantityBase - SUM(Child.StoreOrderLine.QuantityBase).**

> **Then if we have the following documents:**
>
> Parent.StoreOrderLine  - StandardQuantityBase = **10.00 PCS**, QuantityBase = **10.00 PCS**
>
> Child.TransactionLine1  - StandardQuantityBase = **4.00 PCS**, QuantityBase = **4.00 PCS**

> **And we are creating a new Child.TransactionLine2 by a generation procedure from the same parent, then the procedure will create:**
>
> Child.TransactionLine2  - StandardQuantityBase = REMAINING(Quantity) = (10.00 PCS - 4.00 PCS) = **6.00 PCS**, QuantityBase = REMAINING(QuantityBase) = (10.00 PCS - 4.00 PCS) = **6.00 PCS**

## New Record

The last column of the metrics table is called "New Record". This column determines whether a new record must be created if the REMAINING() value of the metric is if different from zero. 

Let's imagine that in the previous example:

> Child.TransactionLine1 - StandardQuantityBase = **10.00 PCS**, QuantityBase = **4.00 PCS**

This may be the case if the product in the line is using [Variable (Dynamic) Measurement Ratios](https://confluence.erp.net/display/techdoc/Variable+(Dynamic)+Measurement+Ratios). The ordered StandardQuantityBase is completely fulfilled by the child document the Child.QuantityBase may be bellow or to exceed the QuantityBase ordered by parent document (i.e. REMAINING(QuantityBase) will be different from zero). But we can see that in the table above for the metric MQuantityBase is set "New Record = NO". Which means that in this situation, when the generation procedure is executed - a new record "Child.TransactionLine2" for remaining **6.00 PCS** of QuantityBase **WON'T** be created.