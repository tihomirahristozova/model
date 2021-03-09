# Query Gen_Product_Pictures_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Picture_Id](#product_picture_id)|`uniqueidentifier` `PK`||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Picture_No](#picture_no)|`int` |Unique picture number within the product. Also used for sorting|
|[Comments](#comments)|`nvarchar` ||
|[Picture](#picture)|`varbinary` |The actual product picture. Can be NULL if we insert only some comments|
|[Is_Default](#is_default)|`bit` |1=This is the default picture for the product and the size class; 0=otherwise|
|[Picture_Size_Class](#picture_size_class)|`nvarchar` Allowed: `S`, `L`|Specifies the relative picture size and usage. S=Small picture (thumbnail), L=Large picture (full size), NULL=unspecified.|
|[Last_Update_Time](#last_update_time)|`datetime` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Product_Picture_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Picture_No

| Property | Value |
| - | - |
|Type|int|

### Comments

| Property | Value |
| - | - |
|Type|nvarchar|

### Picture

| Property | Value |
| - | - |
|Type|varbinary|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Picture_Size_Class

| Property | Value |
| - | - |
|Type|nvarchar|

### Last_Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


