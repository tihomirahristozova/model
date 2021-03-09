# Query Gen_Product_Groups_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Parent](#parent)|`nvarchar` ||
|[Product_Group_Name](#product_group_name)|`nvarchar` `ML`||
|[Product_Group_Code](#product_group_code)|`nvarchar` ||
|[Full_Path](#full_path)|`nvarchar` ||
|[Notes](#notes)|`nvarchar` ||
|[Next_Part_Number](#next_part_number)|`nvarchar` ||
|[Product_Name_Mask](#product_name_mask)|`nvarchar` `ML`||
|[Product_Description_Mask](#product_description_mask)|`nvarchar` `ML`||
|[Configurator_Status](#configurator_status)|`tinyint` Allowed: `0`, `1`, `2`||
|[Configurator_Creates_Recipe](#configurator_creates_recipe)|`bit` ||
|[Default_Product_Type_Id](#default_product_type_id)|`uniqueidentifier` ||
|[Default_Measurement_Unit_Id](#default_measurement_unit_id)|`uniqueidentifier` ||
|[Pricing_Model_Id](#pricing_model_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When not NULL, specifies that the product group, its sub-groups and products are specific to a given enterprise company and may be used only in documents from this enterprise company.|
|[Next_Serial_Number](#next_serial_number)|`nvarchar` |When not NULL, specifies the next serial number, that should be assigned to new produced items.|
|[Active](#active)|`bit` |1 if the product group is active, 0 - not to list in combo boxes for choosing in new documents|
|[Use_Lots](#use_lots)|`nvarchar` Allowed: `A`, `N`, `R`, Readonly|Specifies whether for the products from this group and its sub-groups the use of lots in store documents is required or is unallowed or is allowed while not required.|
|[Picture_Last_Update_Time](#picture_last_update_time)|`datetime` Readonly||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Full_Path

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Next_Part_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Name_Mask

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Description_Mask

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Use_Lots

| Property | Value |
| - | - |
|Type|nvarchar|

### Picture_Last_Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


