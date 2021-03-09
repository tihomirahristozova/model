# Procedure Gen_Document_Amounts_Table_Load_By_Document_Id


## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Amount_Id](#document_amount_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Document_Amount_Type_Id](#document_amount_type_id)|`uniqueidentifier` |The type of the amount.|
|[Input_Percent](#input_percent)|`decimal(7, 6)` |When not null, specifies that the amount for this document will be calculated as percent of the base amounts (which are defined in the amount type).|
|[Input_Amount](#input_amount)|`decimal(14, 2)` |When not null, specifies directly the amount of the additional amount.|
|[Input_Amount_Currency_Id](#input_amount_currency_id)|`uniqueidentifier` |When specifying the amount directly in Input Amount, this contains the currency of the amount. Used and required when Input Amount is not null.|
|[User_Can_Change_Input](#user_can_change_input)|`bit` |1 if the user, entering the document is allowed to change the default input percent|
|[Input_Unit_Amount](#input_unit_amount)|`decimal(14, 5)` |Input unit amount for the calculation of the current amount.|
|[Input_Unit_Id](#input_unit_id)|`uniqueidentifier` |Measurement unit of the input unit amount.|
|[Row_Version](#row_version)|`timestamp` ||
|[Base_Amount](#base_amount)|`decimal(0, 0)` Readonly|The calculated base amount (in documents currency) from the last document amount recalculation. The base amount is the base, over which the additional amounts are calculated. Null if the amount is not distributed yet.|
|[Total_Distributed_Amount](#total_distributed_amount)|`decimal(0, 0)` Readonly|The total amount (in documents currency) which was distributed to the documents lines. Null if the amount is not distributed yet.|
|[Amount_Type_Code](#amount_type_code)|`nvarchar` Readonly||
|[Description](#description)|`nvarchar` Readonly||

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
|Type|decimal(7, 6)|

### Input_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

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
|Type|decimal(14, 5)|

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

### Amount_Type_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|


