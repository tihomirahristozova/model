# Table Gen_Product_Pictures

Pictures of products. Entity: Gen_Product_Pictures

## Owner Tables Hierarchy

* [Gen_Products](Gen_Products.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Picture_No](#picture_no)|`int` |Unique picture number within the product. Also used for sorting|
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Comments](#comments)|`nvarchar(254)` ||
|[Is_Default](#is_default)|`bit` |1=This is the default picture for the product and the size class; 0=otherwise|
|[Picture](#picture)|`varbinary` |The actual product picture. Can be NULL if we insert only some comments|
|[Product_Picture_Id](#product_picture_id)|`uniqueidentifier` `PK`||
|[Picture_Size_Class](#picture_size_class)|`nvarchar(1)` Allowed: `S`, `L`|Specifies the relative picture size and usage. S=Small picture (thumbnail), L=Large picture (full size), NULL=unspecified.|
|[Last_Update_Time](#last_update_time)|`datetime` Readonly|The exact server time, when the picture was last updated. Set automatically.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Picture_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Comments

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Picture

| Property | Value |
| - | - |
|Type|varbinary|

### Product_Picture_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Picture_Size_Class

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Last_Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


