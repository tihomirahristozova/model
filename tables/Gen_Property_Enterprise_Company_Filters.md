# Table Gen_Property_Enterprise_Company_Filters

Provides a way to apply different filtering of the property allowed values for the different enterprise companies. Entity: Gen_Property_Enterprise_Company_Filters

## Owner Tables Hierarchy

* [Gen_Properties](Gen_Properties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Property_Enterprise_Company_Filter_Id](#property_enterprise_company_filter_id)|`uniqueidentifier` `PK`||
|[Property_Id](#property_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company for which the current filter is specifed.|
|[Filter_Xml](#filter_xml)|`nvarchar(2147483647)` |When not null, specifies a filter for the allowed values of the property for the specified enterprise company.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Property_Enterprise_Company_Filter_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Filter_Xml

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


