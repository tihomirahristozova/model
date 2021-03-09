# Query Gen_Product_Variants_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` `PK`||
|[Product_Id](#product_id)|`uniqueidentifier` |The product for which this variant is defined.|
|[Product_Variant_Code](#product_variant_code)|`nvarchar` Readonly|The code of the variant. The code is unique within the Product.|
|[Variant_Color_Id](#variant_color_id)|`uniqueidentifier` |The color of the variant. NULL means that the variant does not have a specific color.|
|[Variant_Size_Id](#variant_size_id)|`uniqueidentifier` |The size of the variant. NULL means that the variant does not have a specific size.|
|[Variant_Style_Id](#variant_style_id)|`uniqueidentifier` |The style of the variant. NULL means that the variant does not have a specific style.|
|[Bar_Code](#bar_code)|`nvarchar` |When specified, it contains a bar code which uniquely identifies the product variant.|
|[Product_Variant_Name](#product_variant_name)|`nvarchar` `ML`, Readonly|Product variant name. It is the concatenation of the names of the color, size and style.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Variant_Color_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Variant_Size_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Variant_Style_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bar_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Variant_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


