# Table Acc_Templates

Accounting templates are used to automate the postings for repetitive business transactions. Templates can be bound to almost all documents and automate their postings. Entity: Acc_Templates

## Owner Tables Hierarchy

* [Wf_Routes](Wf_Routes.md)
* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Template_Id](#template_id)|`uniqueidentifier` `PK`||
|[Template_Name](#template_name)|`nvarchar(254)` ||
|[Route_Id](#route_id)|`uniqueidentifier` |The route which activates the template|
|[Voucher_Date_Source](#voucher_date_source)|`nvarchar(2000)` |Determines the source for the document date of the generated voucher. If not specified the voucher date is set as usual.|
|[Voucher_Description_Mask](#voucher_description_mask)|`nvarchar(2147483647)` |Template voucher description. Can use field substitutes, surrounded with square brackets|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Template_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Route_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Voucher_Date_Source

| Property | Value |
| - | - |
|Type|nvarchar(2000)|

### Voucher_Description_Mask

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


