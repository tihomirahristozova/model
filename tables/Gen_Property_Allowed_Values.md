# Table Gen_Property_Allowed_Values

User-defined properties allowed values. Can be specified only for properties with unbound allowed values (e.g. for which Allowed Values Entity is not set). Entity: Gen_Property_Allowed_Values

## Owner Tables Hierarchy

* [Gen_Properties](Gen_Properties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Property_Allowed_Value_Id](#property_allowed_value_id)|`uniqueidentifier` `PK`||
|[Property_Id](#property_id)|`uniqueidentifier` ||
|[Property_Allowed_Value](#property_allowed_value)|`nvarchar(254)` |The actual allowed value.|
|[Description](#description)|`nvarchar(254)` `ML`|The description of the property allowed value. Used to fill the Description column of the Property_Value in Gen_Property_Values_Table.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Active](#active)|`bit` |Specifies whether the allowed value is active and can be used when selecting property values.|
|[Picture](#picture)|`varbinary` |When not null, specifies a picture representation of the allowed value.|
|[Long_Description](#long_description)|`nvarchar(2147483647)` |When not null, specifies a long description of the allowed value. This long description is only used as helper information when selecting values, it is not copied in the property value.|
|[Parent_Allowed_Value_Id](#parent_allowed_value_id)|`uniqueidentifier` |The value of the parent property, for which this allowed value is valid.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Property_Allowed_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Allowed_Value

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Picture

| Property | Value |
| - | - |
|Type|varbinary|

### Long_Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Parent_Allowed_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


