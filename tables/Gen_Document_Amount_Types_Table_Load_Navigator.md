# Query Gen_Document_Amount_Types_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` `PK`||
|[Amount_Type_Name](#amount_type_name)|`nvarchar` `ML`||
|[Amount_Type_Code](#amount_type_code)|`nvarchar` ||
|[Description](#description)|`nvarchar` ||
|[Amount_Input_Allowed](#amount_input_allowed)|`bit` ||
|[Percent_Input_Allowed](#percent_input_allowed)|`bit` ||
|[Distribute_By](#distribute_by)|`nvarchar` Allowed: `AMOUNT`, `MEASUREMENT`, `PRODUCT DEFINITION`||
|[Default_Percent](#default_percent)|`decimal(0, 0)` ||
|[Distribute_By_Measurement_Category_Id](#distribute_by_measurement_category_id)|`uniqueidentifier` ||
|[Add_To_Customer](#add_to_customer)|`bit` ||
|[Add_To_Line](#add_to_line)|`bit` ||
|[Base_On_Lines](#base_on_lines)|`bit` ||
|[Round_Scale](#round_scale)|`int` ||
|[Is_Active](#is_active)|`bit` ||
|[Allowed_Directions](#allowed_directions)|`int` Allowed: `-1`, `0`, `1`||

## Columns

### Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Amount_Type_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Amount_Input_Allowed

| Property | Value |
| - | - |
|Type|bit|

### Percent_Input_Allowed

| Property | Value |
| - | - |
|Type|bit|

### Distribute_By

| Property | Value |
| - | - |
|Type|nvarchar|

### Default_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Distribute_By_Measurement_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Add_To_Customer

| Property | Value |
| - | - |
|Type|bit|

### Add_To_Line

| Property | Value |
| - | - |
|Type|bit|

### Base_On_Lines

| Property | Value |
| - | - |
|Type|bit|

### Round_Scale

| Property | Value |
| - | - |
|Type|int|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Allowed_Directions

| Property | Value |
| - | - |
|Type|int|


