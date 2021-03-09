# Query Scm_Requisition_Lines_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Requisition_Line_Id](#requisition_line_id)|`uniqueidentifier` `PK`||
|[Display_Column](#display_column)|`nvarchar` ||
|[Part_Number](#part_number)|`nvarchar` |Unique part number of the product|
|[Product_Description](#product_description)|`nvarchar` `ML`|The description of the required product. When Product is set, this is copied initially from the product name. When Product is null, this contains the manually entered description of the desired product.|

## Columns

### Requisition_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Display_Column

| Property | Value |
| - | - |
|Type|nvarchar|

### Part_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Description

| Property | Value |
| - | - |
|Type|nvarchar|


