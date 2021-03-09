# Table Crm_Sales_Order_Promotional_Packages

The promotional packages, included in a sales order. Entity: Crm_Sales_Order_Promotional_Packages

## Owner Tables Hierarchy

* [Crm_Sales_Orders](Crm_Sales_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sales_Order_Promotional_Package_Id](#sales_order_promotional_package_id)|`uniqueidentifier` `PK`||
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` ||
|[Promotional_Package_Id](#promotional_package_id)|`uniqueidentifier` |The type of promotional package sold|
|[Number_Of_Packages](#number_of_packages)|`int` |Number of packages sold|
|[Line_Number](#line_number)|`int` |Consecutive line number of the package, unique within the document.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sales_Order_Promotional_Package_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Promotional_Package_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Number_Of_Packages

| Property | Value |
| - | - |
|Type|int|

### Line_Number

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


