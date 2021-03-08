# Table Crm_Sales_Order_Payment_Orders_Templates

Contains options for generation of payment orders. Each option set is assigned to specific generation route. Entity: Crm_Sales_Order_Payment_Orders_Templates

# Aggregate Hierarchy

* [Wf_Routes](Wf_Routes.md)
* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Create_For_Invoiced_Amounts|`Boolean`||True to add to the payment order, the part of the amount of the sales order, which is invoiced. `Required` |
|Create_For_Not_Invoiced_Amounts|`Boolean`||True to add to the payment order, the part of the amount of the sales order, which is not included in any invoice. `Required` |
|Is_Amount_With_VAT|`Boolean`||True to indicate that the parent document includes VAT and the generated the payment order should be with Is Amount With VAT = true. This setting DOES NOT affect whether the generated amount should include VAT or not, it simply sets the flag in the generated order. `Required` |
|Update_For_Invoices|`Boolean`||Update the payment order when invoices are issued for any of the sales orders lines. `Required` |
