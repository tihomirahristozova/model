# Table Gen_Party_Bank_Accounts

The bank accounts of a party. Entity: Gen_Party_Bank_Accounts

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Party_Bank_Account_Id](#party_bank_account_id)|`uniqueidentifier` `PK`||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Bank_Code](#bank_code)|`nvarchar(30)` |The code of the bank, usually the BIC code|
|[Bank_Name](#bank_name)|`nvarchar(100)` `ML`|The full name of the bank|
|[Bank_Branch_Name](#bank_branch_name)|`nvarchar(100)` `ML`|The name of the branch office of the bank, where the account is located. Required (not-null) only for own accounts for printing or exporting bank payments|
|[Bank_Address](#bank_address)|`nvarchar(254)` `ML`|The address of the bank or the bank branch office. Required (not-null) only for own accounts for printing or exporting bank payments|
|[Bank_Account_Code](#bank_account_code)|`nvarchar(50)` |The code of the account, usually the IBAN code|
|[Notes](#notes)|`nvarchar(254)` ||
|[Is_Default](#is_default)|`bit` |1 if the this is the default account for the party. Only one default per party is allowed|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Party_Bank_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bank_Code

| Property | Value |
| - | - |
|Type|nvarchar(30)|

### Bank_Name

| Property | Value |
| - | - |
|Type|nvarchar(100)|

### Bank_Branch_Name

| Property | Value |
| - | - |
|Type|nvarchar(100)|

### Bank_Address

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Bank_Account_Code

| Property | Value |
| - | - |
|Type|nvarchar(50)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


