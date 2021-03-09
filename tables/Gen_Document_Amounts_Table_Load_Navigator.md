# Query Gen_Document_Amounts_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Amount_Id](#document_amount_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` ||
|[Input_Percent](#input_percent)|`decimal(0, 0)` ||
|[Input_Amount](#input_amount)|`decimal(0, 0)` ||
|[Input_Amount_Currency_Id](#input_amount_currency_id)|`uniqueidentifier` ||
|[User_Can_Change_Input](#user_can_change_input)|`bit` ||
|[Input_Unit_Amount](#input_unit_amount)|`decimal(0, 0)` |Input unit amount for the calculation of the current amount.|
|[Input_Unit_Id](#input_unit_id)|`uniqueidentifier` |Measurement unit of the input unit amount.|
|[Row_Version](#row_version)|`timestamp` ||
|[Base_Amount](#base_amount)|`decimal(0, 0)` Readonly|The calculated base amount (in documents currency) from the last document amount recalculation. The base amount is the base, over which the additional amounts are calculated. Null if the amount is not distributed yet.|
|[Total_Distributed_Amount](#total_distributed_amount)|`decimal(0, 0)` Readonly|The total amount (in documents currency) which was distributed to the documents lines. Null if the amount is not distributed yet.|
|[Base](#base)|`decimal(0, 0)` ||
|[Amount](#amount)|`decimal(0, 0)` ||
|[Total](#total)|`decimal(0, 0)` ||

## Columns

### Document_Amount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Input_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Input_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Input_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Can_Change_Input

| Property | Value |
| - | - |
|Type|bit|

### Input_Unit_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Input_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Base_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Total_Distributed_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Total

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


