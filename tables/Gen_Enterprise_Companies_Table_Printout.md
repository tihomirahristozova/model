# Procedure Gen_Enterprise_Companies_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` `PK`||
|[Company_Id](#company_id)|`uniqueidentifier` |Contains the base company data on which this enterprise company is based.|
|[Company_Name](#company_name)|`nvarchar` `ML`|The name of the party|
|[Party_Id](#party_id)|`uniqueidentifier` |Base party Id|
|[Registration_Type](#registration_type)|`nvarchar` `ML`|Legal registration type - like LTD., PLC, etc. NULL means unknown|
|[Registration_Number](#registration_number)|`nvarchar` |Unique, government-assigned registration number. NULL means unknown|
|[Registration_VAT_Number](#registration_vat_number)|`nvarchar` |VAT registration number where applicable. NULL means that VAT number is not applicable or unknown|
|[Responsible_Person_Name](#responsible_person_name)|`nvarchar` `ML`|Primary responsible person of the company. NULL means unknown.|
|[Registration_Responsible_Person_Id](#registration_responsible_person_id)|`uniqueidentifier` |The personal record of the primary responsible person as per registration. NULL means unknown|
|[Registration_Responsible_Person_Name](#registration_responsible_person_name)|`nvarchar` `ML`|The name of the party|
|[Registration_Primary_Address](#registration_primary_address)|`nvarchar` `ML`|The primary registration address of the company.|
|[Country_Id](#country_id)|`uniqueidentifier` |The country, where the company is registered.|
|[Country_Name](#country_name)|`nvarchar` `ML`|Name of the country|
|[City](#city)|`nvarchar` `ML`|The city in which the company is registered.|
|[Base_Currency_Id](#base_currency_id)|`uniqueidentifier` |The base currency for summary reporting for this company.|
|[Base_Currency_Name](#base_currency_name)|`nvarchar` ||
|[Base_Currency_Sign](#base_currency_sign)|`nvarchar` |The international currency designator, as defined in ISO 4217. For example euro is represented as 'EUR'.|
|[Default_Costing_Method](#default_costing_method)|`nvarchar` Allowed: `AVG`, `EXP`, `BLD`|Default method for cost evaluation (if not specified in the product). Currently supported: EXP - Explicit lot specifying; AVG - Average cost|
|[Default_Language](#default_language)|`nvarchar` Allowed: `bg`, `en`|The default language for multi-language names in the definitions (like Customer_Name, Product_Name, ...).|
|[Exchange_Difference_Debit_Account_Id](#exchange_difference_debit_account_id)|`uniqueidentifier` |Account for balancing accounting vouchers with debit difference due to currency exchanges|
|[Exchange_Difference_Credit_Account_Id](#exchange_difference_credit_account_id)|`uniqueidentifier` |Account for balancing accounting vouchers with credit difference due to currency exchanges|
|[Advance_Product_Id](#advance_product_id)|`uniqueidentifier` |Product that is used for handling advances in trade documents.|
|[VAT_Document_Amount_Type_Id](#vat_document_amount_type_id)|`uniqueidentifier` |The document amount that is used to determine the amount of the VAT entries when they are generated.|
|[Bank_Code](#bank_code)|`nvarchar` |The code of the bank, usually the BIC code|
|[Bank_Name](#bank_name)|`nvarchar` `ML`|The full name of the bank|
|[Bank_Branch_Name](#bank_branch_name)|`nvarchar` `ML`|The name of the branch office of the bank, where the account is located. Required (not-null) only for own accounts for printing or exporting bank payments|
|[Bank_Address](#bank_address)|`nvarchar` `ML`|The address of the bank or the bank branch office. Required (not-null) only for own accounts for printing or exporting bank payments|
|[Bank_Account_Code](#bank_account_code)|`nvarchar` |The code of the account, usually the IBAN code|

## Columns

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Company_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Registration_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Registration_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Registration_VAT_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Responsible_Person_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Registration_Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Registration_Responsible_Person_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Registration_Primary_Address

| Property | Value |
| - | - |
|Type|nvarchar|

### Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Country_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### City

| Property | Value |
| - | - |
|Type|nvarchar|

### Base_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Base_Currency_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Base_Currency_Sign

| Property | Value |
| - | - |
|Type|nvarchar|

### Default_Costing_Method

| Property | Value |
| - | - |
|Type|nvarchar|

### Default_Language

| Property | Value |
| - | - |
|Type|nvarchar|

### Exchange_Difference_Debit_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Exchange_Difference_Credit_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Advance_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### VAT_Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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


