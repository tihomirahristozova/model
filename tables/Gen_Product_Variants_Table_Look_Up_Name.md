# Query Gen_Product_Variants_Table_Look_Up_Name


## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` `PK`||
|[Product_Variant_Name](#product_variant_name)|`nvarchar` `ML`, Readonly|Product variant name. It is the concatenation of the names of the color, size and style.|
|[Product_Variant_Code](#product_variant_code)|`nvarchar` Readonly|The code of the variant. The code is unique within the Product. It is the concatenation of the codes of the color, size and style.|

## Columns

### Product_Variant_Id


Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Gen_Product_Variants](Gen_Product_Variants.md).[Product_Variant_Id](Gen_Product_Variants.md#product_variant_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Product_Variant_Name


Product_Variant_Name


Product variant name. It is the concatenation of the names of the color, size and style.


Product variant name. It is the concatenation of the names of the color, size and style.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Variants](Gen_Product_Variants.md).[Product_Variant_Name](Gen_Product_Variants.md#product_variant_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Product_Variant_Code


Product_Variant_Code


The code of the variant. The code is unique within the Product. It is the concatenation of the codes of the color, size and style.


The code of the variant. The code is unique within the Product. It is the concatenation of the codes of the color, size and style.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Variants](Gen_Product_Variants.md).[Product_Variant_Code](Gen_Product_Variants.md#product_variant_code)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|


