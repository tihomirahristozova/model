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

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Product_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(180)|

### Product_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Next_Part_Number

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Product_Name_Mask

| Property | Value |
| - | - |
|Type|nvarchar(1000)|

### Product_Description_Mask

| Property | Value |
| - | - |
|Type|nvarchar(1000)|

### Configurator_Status

| Property | Value |
| - | - |
|Type|tinyint|

### Configurator_Creates_Recipe

| Property | Value |
| - | - |
|Type|bit|

### Default_Product_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pricing_Model_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Next_Serial_Number

| Property | Value |
| - | - |
|Type|nvarchar(40)|

### Picture

| Property | Value |
| - | - |
|Type|varbinary|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Use_Lots

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Picture_Last_Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


