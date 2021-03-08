# Table Gen_Product_Pictures

Pictures of products. Entity: Gen_Product_Pictures

# Aggregate Hierarchy

* [Gen_Products](Gen_Products.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Product_Picture_Id|`Guid`|`PK`, Readonly||
|Comments|`String`||Comments for this ProductPicture. |
|Is_Default|`Boolean`||True=This is the default picture for the product and the size class; false=otherwise. `Required` `Default(false)` `Filter(eq)` |
|Last_Update_Time|`DateTime?`|Readonly|The exact server time, when the picture was last updated. Set automatically. `Filter(ge;le)` `ReadOnly` |
|Picture|`Byte[]`|`BLOB`|The actual product picture. Can be null if we insert only some comments. |
|Picture_No|`Int32`||Unique picture number within the product. Also used for sorting. `Required` `Filter(eq;like)` |
|Picture_Size_Class|`PictureSizeClass?`|Allowed: `S`, `L`|Specifies the relative picture size and usage. S=Small picture (thumbnail), L=Large picture (full size), null=unspecified. |
