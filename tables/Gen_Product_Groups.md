# Table Gen_Product_Groups

Hierarchical categorization of the products. Entity: Gen_Product_Groups

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique Id of the item group|
|[Parent](#parent)|`nvarchar(254)` |Full tree path of the parent group in the form /parent/.../leaf/. Contains the group names.|
|[Product_Group_Name](#product_group_name)|`nvarchar(180)` `ML`|Group name should be unique among the other groups within the same parent|
|[Product_Group_Code](#product_group_code)|`nvarchar(16)` ||
|[Full_Path](#full_path)|`nvarchar(254)` |Full tree path in the form /parent/.../leaf/. Contains the group names.|
|[Notes](#notes)|`nvarchar(254)` |User notes for the item group|
|[Next_Part_Number](#next_part_number)|`nvarchar(16)` |Contains the next part number to be auto-assigned to parts, created in the group or sub-groups|
|[Product_Name_Mask](#product_name_mask)|`nvarchar(1000)` `ML`|When not NULL specifies mask for new product names for this group and its sub-groups. The mask substitutes {0}..{n} with the appropriate custom attributes|
|[Product_Description_Mask](#product_description_mask)|`nvarchar(1000)` `ML`|When not NULL specifies mask for new product descriptions for this group and its sub-groups. The mask substitutes {0}..{n} with the appropriate custom attributes|
|[Configurator_Status](#configurator_status)|`tinyint` Allowed: `0`, `1`, `2`|Usage of product configurator for new products. 0=Product configurator cannot be used to create products in this group;1=The configurator can be used;2=The configurator should be used and products cannot be created directly|
|[Configurator_Creates_Recipe](#configurator_creates_recipe)|`bit` |Whether the product configurator should create one default recipe. 1=yes;0=no|
|[Default_Product_Type_Id](#default_product_type_id)|`uniqueidentifier` |When not null, specifies default product type, which should be assigned to new products in the group.|
|[Default_Measurement_Unit_Id](#default_measurement_unit_id)|`uniqueidentifier` |When not null, specifies default measurement unit, which should be assigned to new products in the group.|
|[Pricing_Model_Id](#pricing_model_id)|`uniqueidentifier` |When not null, specifies the pricing model, for the products in this product group. The model is by default valid also for sub-groups, unless they have other models.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When not NULL, specifies that the product group, its sub-groups and products are specific to a given enterprise company and may be used only in documents from this enterprise company.|
|[Next_Serial_Number](#next_serial_number)|`nvarchar(40)` |When not NULL, specifies the next serial number, that should be assigned to new produced items.|
|[Picture](#picture)|`varbinary` |The picture of the product group|
|[Active](#active)|`bit` |1 if the product group is active, 0 - not to list in combo boxes for choosing in new documents|
|[Use_Lots](#use_lots)|`nvarchar(1)` Allowed: `A`, `N`, `R`|Specifies whether for the products from this group and its sub-groups the use of lots in store documents is required or is unallowed or is allowed while not required.|
|[Picture_Last_Update_Time](#picture_last_update_time)|`datetime` Readonly|Last update time of the Picture|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id


Id


Unique Id of the item group


Unique Id of the item group

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
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Id](Gen_Product_Groups.md#id)|
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

### Parent


Parent


Full tree path of the parent group in the form /parent/.../leaf/. Contains the group names.


Full tree path of the parent group in the form /parent/.../leaf/. Contains the group names.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|/|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Parent](Gen_Product_Groups.md#parent)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Product_Group_Name


Product_Group_Name


Group name should be unique among the other groups within the same parent


Group name should be unique among the other groups within the same parent

| Property | Value |
| - | - |
|Type|nvarchar(180)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Product_Group_Name](Gen_Product_Groups.md#product_group_name)|
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
|Max Length|180|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Product_Group_Code


Product_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Product_Group_Code](Gen_Product_Groups.md#product_group_code)|
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
|Max Length|16|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Full_Path


Full_Path


Full tree path in the form /parent/.../leaf/. Contains the group names.


Full tree path in the form /parent/.../leaf/. Contains the group names.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value||
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Full_Path](Gen_Product_Groups.md#full_path)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|yes|

### Notes


Notes


User notes for the item group


User notes for the item group

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Notes](Gen_Product_Groups.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Next_Part_Number


Next_Part_Number


Contains the next part number to be auto-assigned to parts, created in the group or sub-groups


Contains the next part number to be auto-assigned to parts, created in the group or sub-groups

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Next_Part_Number](Gen_Product_Groups.md#next_part_number)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|16|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Product_Name_Mask


Product_Name_Mask


When not NULL specifies mask for new product names for this group and its sub-groups. The mask substitutes {0}..{n} with the appropriate custom attributes


When not NULL specifies mask for new product names for this group and its sub-groups. The mask substitutes {0}..{n} with the appropriate custom attributes

| Property | Value |
| - | - |
|Type|nvarchar(1000)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Product_Name_Mask](Gen_Product_Groups.md#product_name_mask)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|1000|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Product_Description_Mask


Product_Description_Mask


When not NULL specifies mask for new product descriptions for this group and its sub-groups. The mask substitutes {0}..{n} with the appropriate custom attributes


When not NULL specifies mask for new product descriptions for this group and its sub-groups. The mask substitutes {0}..{n} with the appropriate custom attributes

| Property | Value |
| - | - |
|Type|nvarchar(1000)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Product_Description_Mask](Gen_Product_Groups.md#product_description_mask)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|1000|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Configurator_Status


Configurator_Status


Usage of product configurator for new products. 0=Product configurator cannot be used to create products in this group;1=The configurator can be used;2=The configurator should be used and products cannot be created directly


Usage of product configurator for new products. 0=Product configurator cannot be used to create products in this group;1=The configurator can be used;2=The configurator should be used and products cannot be created directly

| Property | Value |
| - | - |
|Type|tinyint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`0`, `1`, `2`|
|Default Value|0|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Configurator_Status](Gen_Product_Groups.md#configurator_status)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Configurator_Creates_Recipe


Configurator_Creates_Recipe


Whether the product configurator should create one default recipe. 1=yes;0=no


Whether the product configurator should create one default recipe. 1=yes;0=no

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Configurator_Creates_Recipe](Gen_Product_Groups.md#configurator_creates_recipe)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Default_Product_Type_Id


Default_Product_Type_Id


When not null, specifies default product type, which should be assigned to new products in the group.


When not null, specifies default product type, which should be assigned to new products in the group.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Product_Types](Gen_Product_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Default_Product_Type_Id](Gen_Product_Groups.md#default_product_type_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Default_Measurement_Unit_Id


Default_Measurement_Unit_Id


When not null, specifies default measurement unit, which should be assigned to new products in the group.


When not null, specifies default measurement unit, which should be assigned to new products in the group.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Default_Measurement_Unit_Id](Gen_Product_Groups.md#default_measurement_unit_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Pricing_Model_Id


Pricing_Model_Id


When not null, specifies the pricing model, for the products in this product group. The model is by default valid also for sub-groups, unless they have other models.


When not null, specifies the pricing model, for the products in this product group. The model is by default valid also for sub-groups, unless they have other models.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Pricing_Models](Crm_Pricing_Models.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Pricing_Model_Id](Gen_Product_Groups.md#pricing_model_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Enterprise_Company_Id


Enterprise_Company_Id


When not NULL, specifies that the product group, its sub-groups and products are specific to a given enterprise company and may be used only in documents from this enterprise company.


When not NULL, specifies that the product group, its sub-groups and products are specific to a given enterprise company and may be used only in documents from this enterprise company.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Enterprise_Company_Id](Gen_Product_Groups.md#enterprise_company_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|

### Next_Serial_Number


Next_Serial_Number


When not NULL, specifies the next serial number, that should be assigned to new produced items.


When not NULL, specifies the next serial number, that should be assigned to new produced items.

| Property | Value |
| - | - |
|Type|nvarchar(40)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Next_Serial_Number](Gen_Product_Groups.md#next_serial_number)|
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
|Max Length|40|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Picture


Picture


The picture of the product group


The picture of the product group

| Property | Value |
| - | - |
|Type|varbinary|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Picture](Gen_Product_Groups.md#picture)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|yes|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Active


Active


1 if the product group is active, 0 - not to list in combo boxes for choosing in new documents


1 if the product group is active, 0 - not to list in combo boxes for choosing in new documents

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Active](Gen_Product_Groups.md#active)|
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

### Use_Lots


Use_Lots


Specifies whether for the products from this group and its sub-groups the use of lots in store documents is required or is unallowed or is allowed while not required.


Specifies whether for the products from this group and its sub-groups the use of lots in store documents is required or is unallowed or is allowed while not required.

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`A`, `N`, `R`|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Use_Lots](Gen_Product_Groups.md#use_lots)|
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
|Max Length|1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Picture_Last_Update_Time


Picture_Last_Update_Time


Last update time of the Picture


Last update time of the Picture

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Picture_Last_Update_Time](Gen_Product_Groups.md#picture_last_update_time)|
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
|GreaterThanOrLessThan|None|yes|yes|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Groups](Gen_Product_Groups.md).[Row_Version](Gen_Product_Groups.md#row_version)|
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
|Supports EQUALS_IN|no|


