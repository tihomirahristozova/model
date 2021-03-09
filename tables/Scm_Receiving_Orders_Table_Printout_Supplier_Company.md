# Procedure Scm_Receiving_Orders_Table_Printout_Supplier_Company


## Summary

| Name | Type | Description |
| - | - | --- |
|[Company_Id](#company_id)|`uniqueidentifier` `PK`|Unique company Id|
|[Party_Id](#party_id)|`uniqueidentifier` |Base party Id|
|[Party_Id_Text](#party_id_text)|`nvarchar` `ML`|The name of the party|
|[Registration_Type](#registration_type)|`nvarchar` `ML`|Legal registration type - like LTD., PLC, etc. NULL means unknown|
|[Registration_Number](#registration_number)|`nvarchar` |Unique, government-assigned registration number. NULL means unknown|
|[Registration_VAT_Number](#registration_vat_number)|`nvarchar` |VAT registration number where applicable. NULL means that VAT number is not applicable or unknown|
|[Responsible_Person_Name](#responsible_person_name)|`nvarchar` `ML`|Primary responsible person of the company. NULL means unknown.|
|[Registration_Responsible_Person_Id](#registration_responsible_person_id)|`uniqueidentifier` |The personal record of the primary responsible person as per registration. NULL means unknown|
|[Registration_Responsible_Person_Id_Text](#registration_responsible_person_id_text)|`nvarchar` `ML`||
|[Registration_Primary_Address](#registration_primary_address)|`nvarchar` `ML`|The primary registration address of the company.|
|[Country_Id](#country_id)|`uniqueidentifier` |The country, where the company is registered.|
|[Country_Id_Text](#country_id_text)|`nvarchar` `ML`|Name of the country|
|[City](#city)|`nvarchar` `ML`|The city in which the company is registered.|
|[Bank_Code](#bank_code)|`nvarchar` |The code of the bank, usually the BIC code|
|[Bank_Name](#bank_name)|`nvarchar` `ML`|The full name of the bank|
|[Bank_Branch_Name](#bank_branch_name)|`nvarchar` `ML`|The name of the branch office of the bank, where the account is located. Required (not-null) only for own accounts for printing or exporting bank payments|
|[Bank_Address](#bank_address)|`nvarchar` `ML`|The address of the bank or the bank branch office. Required (not-null) only for own accounts for printing or exporting bank payments|
|[Bank_Account_Code](#bank_account_code)|`nvarchar` |The code of the account, usually the IBAN code|

## Columns

### Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

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

### Registration_Responsible_Person_Id_Text

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

### Country_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### City

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


