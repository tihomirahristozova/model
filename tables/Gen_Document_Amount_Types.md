# Table Gen_Document_Amount_Types

Represents the different types of additional amounts which are calculated for the documents. Entity: Gen_Document_Amount_Types

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` `PK`||
|[Amount_Type_Code](#amount_type_code)|`nvarchar(16)` |A code that can be used to uniquely identify the additional amount. Can also be used for sorting purposes|
|[Amount_Type_Name](#amount_type_name)|`nvarchar(128)` `ML`|The name of the amount type.|
|[Description](#description)|`nvarchar(254)` ||
|[Amount_Input_Allowed](#amount_input_allowed)|`bit` |1 when the user is allowed to input fixed amount for distribution|
|[Percent_Input_Allowed](#percent_input_allowed)|`bit` |1 when the user is allowed to input percent of total for distribution|
|[Distribute_By](#distribute_by)|`nvarchar(20)` Allowed: `AMOUNT`, `MEASUREMENT`, `PRODUCT DEFINITION`|Specifies how the amount will be distributed among the document lines. Valid values are: ('AMOUNT','MEASUREMENT','PRODUCT DEFINITION')|
|[Default_Percent](#default_percent)|`decimal(7, 6)` |Default percent for amounts for which percent input is allowed; NULL otherwise|
|[Distribute_By_Measurement_Category_Id](#distribute_by_measurement_category_id)|`uniqueidentifier` |Specifies the measurement category to be used for distribution, when the Distribute_By = 'MEASUREMENT'|
|[Add_To_Customer](#add_to_customer)|`bit` |1 means that the amount will be charged to the primary customer of the document|
|[Add_To_Line](#add_to_line)|`bit` |1 means that the resulting amount will be added to the amount of each respective line|
|[Base_On_Lines](#base_on_lines)|`bit` |1 means that the percentages will be applied over lines plus dependant amounts; 0 means only dependant amounts|
|[Round_Scale](#round_scale)|`int` |The amounts should be rounded with the specified number of digits after the decimal point. NULL means to use the currency default|
|[Is_Active](#is_active)|`bit` |1 when the amount type is active for new records; 0 - otherwise|
|[Allowed_Directions](#allowed_directions)|`int` Allowed: `-1`, `0`, `1`|Specifies condition for the sign of the allowed values for input percent or amount ​​that can be set in the documents.|
|[Unit_Amount_Input_Allowed](#unit_amount_input_allowed)|`bit` |Specifies whether the user is allowed to input fixed unit amount for the calculation of the amount.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount_Type_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Amount_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

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
|Type|nvarchar(20)|

### Default_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

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

### Unit_Amount_Input_Allowed

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


