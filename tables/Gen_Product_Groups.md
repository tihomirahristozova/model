# Table Gen_Product_Groups

Hierarchical categorization of the products. Entity: Gen_Product_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Active|`Boolean`||True if the product group is active, false - not to list in combo boxes for choosing in new documents. `Required` `Default(true)` `Filter(eq)` |
|Product_Group_Code|`String`||The unique code of the ProductGroup. `Required` `Filter(eq;like)` `ORD` |
|Configurator_Creates_Recipe|`Boolean`||Whether the product configurator should create one default recipe. true=yes;false=no. `Required` `Default(false)` |
|Configurator_Status|`ConfiguratorStatus`|Allowed: `0`, `1`, `2`|Usage of product configurator for new products. 0=Product configurator cannot be used to create products in this group;1=The configurator can be used;2=The configurator should be used and products cannot be created directly. `Required` `Default(0)` |
|Full_Path|`String`||Full tree path in the form /parent/.../leaf/. Contains the group names. `Required` `Default("")` `Filter(eq;like)` `ORD` |
|Product_Group_Name|`MultilanguageString`||Group name should be unique among the other groups within the same parent. `Required` `Filter(eq;like)` |
|Next_Part_Number|`String`||Contains the next part number to be auto-assigned to parts, created in the group or sub-groups. |
|Next_Serial_Number|`String`||When not null, specifies the next serial number, that should be assigned to new produced items. `Filter(eq;like)` |
|Notes|`String`||User notes for the item group. |
|Parent|`String`||Full tree path of the parent group in the form /parent/.../leaf/. Contains the group names. `Required` `Default("/")` `Filter(eq)` `ORD` |
|Picture|`Byte[]`|`BLOB`|The picture of the product group. |
|Picture_Last_Update_Time|`DateTime?`|Readonly|Last update time of the Picture. `Filter(ge;le)` `ReadOnly` |
|Product_Description_Mask|`MultilanguageString`||When not null specifies mask for new product descriptions for this group and its sub-groups. The mask substitutes {0}..{n} with the appropriate custom attributes. |
|Product_Name_Mask|`MultilanguageString`||When not null specifies mask for new product names for this group and its sub-groups. The mask substitutes {0}..{n} with the appropriate custom attributes. |
|Use_Lots|`UseLots?`|Allowed: `A`, `N`, `R`|Specifies whether for the products from this group and its sub-groups the use of lots in store documents is required or is unallowed or is allowed while not required. |
