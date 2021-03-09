# Procedure Acc_Vouchers_Table_Load_Environment_Property_Values_Voucher_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Property_Value_Id](#property_value_id)|`uniqueidentifier` `PK`||
|[Property_Id](#property_id)|`uniqueidentifier` |The property, whose value is stored here.|
|[Entity_Item_Id](#entity_item_id)|`uniqueidentifier` |The Id of the actual entity for which the value is specified.|
|[Property_Value](#property_value)|`nvarchar` |The actual value of the property for the specified entity (the entity with the specified Id).|
|[Description](#description)|`nvarchar` `ML`|The actual description value of the property for the specified entity (the entity with the specified Id).|
|[Picture](#picture)|`varbinary` ||
|[Value_Id](#value_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Property_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|

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


