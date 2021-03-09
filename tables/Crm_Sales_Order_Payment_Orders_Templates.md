# Table Crm_Sales_Order_Payment_Orders_Templates

Contains options for generation of payment orders. Each option set is assigned to specific generation route. Entity: Crm_Sales_Order_Payment_Orders_Templates

## Owner Tables Hierarchy

* [Wf_Routes](Wf_Routes.md)
* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Route_Id](#route_id)|`uniqueidentifier` |The route to which the current option set is assigned.|
|[Is_Amount_With_VAT](#is_amount_with_vat)|`bit` |1 to indicate that the parent document includes VAT and the generated the payment order should be with Is Amount With VAT = 1. This setting DOES NOT affect whether the generated amount should include VAT or not, it simply sets the flag in the generated order.|
|[Update_For_Invoices](#update_for_invoices)|`bit` |Update the payment order when invoices are issued for any of the sales orders lines.|
|[Create_For_Not_Invoiced_Amounts](#create_for_not_invoiced_amounts)|`bit` |1 to add to the payment order, the part of the amount of the sales order, which is not included in any invoice.|
|[Create_For_Invoiced_Amounts](#create_for_invoiced_amounts)|`bit` |1 to add to the payment order, the part of the amount of the sales order, which is invoiced.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Route_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Amount_With_VAT

| Property | Value |
| - | - |
|Type|bit|

### Update_For_Invoices

| Property | Value |
| - | - |
|Type|bit|

### Create_For_Not_Invoiced_Amounts

| Property | Value |
| - | - |
|Type|bit|

### Create_For_Invoiced_Amounts

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


