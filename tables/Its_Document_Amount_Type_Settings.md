# Table Its_Document_Amount_Type_Settings

Specifies the additional amounts, which are added to the invoiced and statistical values. Entity: Its_Document_Amount_Type_Settings

## Owner Tables Hierarchy

* [Gen_Document_Amount_Types](Gen_Document_Amount_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Amount_Type_Setting_Id](#document_amount_type_setting_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company for which the setting is valid|
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` |The amount type which will be added to the invoiced or the statistical value|
|[Add_To_Invoiced_Value](#add_to_invoiced_value)|`bit` |1= to add the amount to the invoiced value, 0=otherwise|
|[Add_To_Statistical_Value](#add_to_statistical_value)|`bit` |1= to add the amount to the statistical value, 0=otherwise|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Amount_Type_Setting_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Add_To_Invoiced_Value

| Property | Value |
| - | - |
|Type|bit|

### Add_To_Statistical_Value

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


