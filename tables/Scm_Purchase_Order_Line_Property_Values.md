# Table Scm_Purchase_Order_Line_Property_Values


## Summary

| Name | Type | Description |
| - | - | --- |
|[Entity_Item_Id](#entity_item_id)|`uniqueidentifier` |The Id of the actual entity for which the value is specified.|
|[Property_Id](#property_id)|`uniqueidentifier` |The property, whose value is stored here.|
|[Property_Value](#property_value)|`nvarchar(254)` |The actual value of the property for the specified entity (the entity with the specified Id).|
|[Description](#description)|`nvarchar(254)` `ML`|The actual description value of the property for the specified entity (the entity with the specified Id).|
|[Property_Value_Id](#property_value_id)|`uniqueidentifier` `PK`||
|[Picture](#picture)|`varbinary` |The actual picture of the property for the specified entity (the entity with the specified Id).|
|[Value_Id](#value_id)|`uniqueidentifier` |The internal Id of the value of the property for the specified entity (the entity with the specified Id). For choosable properties, this contains the id of the original "allowed value" row, from which the value was derived. NULL for non-choosable (free-text) properties, but also for old property values (before this id was available) or other unknown values.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Entity_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Value

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Property_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Picture

| Property | Value |
| - | - |
|Type|varbinary|

### Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


