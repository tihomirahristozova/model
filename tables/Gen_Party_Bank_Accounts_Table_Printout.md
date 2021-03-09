# Procedure Gen_Party_Bank_Accounts_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Party_Bank_Account_Id](#party_bank_account_id)|`uniqueidentifier` `PK`||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Party_Name](#party_name)|`nvarchar` `ML`|The name of the party|
|[Bank_Code](#bank_code)|`nvarchar` |The code of the bank, usually the BIC code|
|[Bank_Name](#bank_name)|`nvarchar` `ML`|The full name of the bank|
|[Bank_Branch_Name](#bank_branch_name)|`nvarchar` `ML`|The name of the branch office of the bank, where the account is located. Required (not-null) only for own accounts for printing or exporting bank payments|
|[Bank_Address](#bank_address)|`nvarchar` `ML`|The address of the bank or the bank branch office. Required (not-null) only for own accounts for printing or exporting bank payments|
|[Bank_Account_Code](#bank_account_code)|`nvarchar` |The code of the account, usually the IBAN code|
|[Notes](#notes)|`nvarchar` ||
|[Is_Default](#is_default)|`bit` |1 if the this is the default account for the party. Only one default per party is allowed|

## Columns

### Party_Bank_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Bank_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Bank_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Bank_Branch_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Bank_Address

| Property | Value |
| - | - |
|Type|nvarchar|

### Bank_Account_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|


