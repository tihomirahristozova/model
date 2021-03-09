# Table Acc_Accounts

Contains the leaf level of the chart of accounts. Entity: Acc_Accounts

## Summary

| Name | Type | Description |
| - | - | --- |
|[Account_Id](#account_id)|`uniqueidentifier` `PK`||
|[Account_Group_Id](#account_group_id)|`uniqueidentifier` |The account group to which this account belongs|
|[Account_Number](#account_number)|`nvarchar(30)` |The number of the account, unique within the account group|
|[Account_Full_Number](#account_full_number)|`nvarchar(30)` Readonly|The full number of the account, unique among all accounts. It consists of the group number, concatenated with the account number|
|[Account_Name](#account_name)|`nvarchar(254)` `ML`|The account name|
|[Description](#description)|`nvarchar(254)` ||
|[Currency_Id](#currency_id)|`uniqueidentifier` |The primary currency of the account. All movements on the account are stored in this currency. If there are movements on the account, the currency cannot be changed|
|[Discontinued](#discontinued)|`bit` |1 means that the account won't be used any more and should not appear in combo boxes|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Currency_Valuation_Method](#currency_valuation_method)|`nvarchar(3)` Allowed: `ACB`, `DCD`, `BRD`|Method for base currency valuation of non base currency amounts. ACB = Account_Current_Balance, DCD = Document_Currency_Directory, BRD=Balance_Reference_Document|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Account_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Account_Number

| Property | Value |
| - | - |
|Type|nvarchar(30)|

### Account_Full_Number

| Property | Value |
| - | - |
|Type|nvarchar(30)|

### Account_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Discontinued

| Property | Value |
| - | - |
|Type|bit|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Valuation_Method

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


