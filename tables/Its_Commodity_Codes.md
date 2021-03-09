# Table Its_Commodity_Codes

Contains the approved Intrastat commodity codes for each period. Entity: Its_Commodity_Codes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Intrastat_Commodity_Code_Id](#intrastat_commodity_code_id)|`uniqueidentifier` `PK`||
|[Commodity_Code](#commodity_code)|`nvarchar(8)` |Product code from the Intrastat Combined nomenclature|
|[Description](#description)|`nvarchar(4000)` `ML`|Description of the product code from the Intrastat Combined nomenclature|
|[Supplementary_Unit](#supplementary_unit)|`nvarchar(16)` |If not null, the related product should have additional measurement unit with the same code as specified in this field. The additional unit will be used for the purposes of the Intrastat declarations|
|[Valid_From](#valid_from)|`date` |The starting date of validity of this code.|
|[Valid_To](#valid_to)|`date` |The ending date of validity of this code.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Intrastat_Commodity_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Commodity_Code

| Property | Value |
| - | - |
|Type|nvarchar(8)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(4000)|

### Supplementary_Unit

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Valid_From

| Property | Value |
| - | - |
|Type|date|

### Valid_To

| Property | Value |
| - | - |
|Type|date|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


