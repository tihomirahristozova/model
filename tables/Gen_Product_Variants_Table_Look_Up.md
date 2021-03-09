# Query Gen_Product_Variants_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` `PK`||
|[Product_Variant_Code](#product_variant_code)|`nvarchar` Readonly|The code of the variant. The code is unique within the Product. It is the concatenation of the codes of the color, size and style.|
|[Bar_Code](#bar_code)|`nvarchar` |When specified, it contains a bar code which uniquely identifies the product variant.|
|[Product_Id](#product_id)|`uniqueidentifier` |The product for which this variant is defined.|
|[Variant_Color_Id](#variant_color_id)|`uniqueidentifier` |The color of the variant. NULL means that the variant does not have a specific color.|
|[Variant_Size_Id](#variant_size_id)|`uniqueidentifier` |The size of the variant. NULL means that the variant does not have a specific size.|
|[Variant_Style_Id](#variant_style_id)|`uniqueidentifier` |The style of the variant. NULL means that the variant does not have a specific style.|

## Columns

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Bar_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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


