# Query Gen_Product_Variants_Table_Look_Up_Name


## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` `PK`||
|[Product_Variant_Name](#product_variant_name)|`nvarchar` `ML`, Readonly|Product variant name. It is the concatenation of the names of the color, size and style.|
|[Product_Variant_Code](#product_variant_code)|`nvarchar` Readonly|The code of the variant. The code is unique within the Product. It is the concatenation of the codes of the color, size and style.|

## Columns

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Variant_Code

| Property | Value |
| - | - |
|Type|nvarchar|


