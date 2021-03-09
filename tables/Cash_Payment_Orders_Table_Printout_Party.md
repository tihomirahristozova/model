# Procedure Cash_Payment_Orders_Table_Printout_Party


## Summary

| Name | Type | Description |
| - | - | --- |
|[Company_Id](#company_id)|`uniqueidentifier` `PK`|Unique company Id|
|[Company_Name](#company_name)|`nvarchar` `ML`||
|[Party_Id](#party_id)|`uniqueidentifier` |Base party Id|
|[Party_Id_Text](#party_id_text)|`nvarchar` `ML`|The name of the party|
|[Registration_Type](#registration_type)|`nvarchar` `ML`|Legal registration type - like LTD., PLC, etc. NULL means unknown|
|[Registration_Number](#registration_number)|`nvarchar` |Unique, government-assigned registration number. NULL means unknown|
|[Registration_VAT_Number](#registration_vat_number)|`nvarchar` |VAT registration number where applicable. NULL means that VAT number is not applicable or unknown|
|[Responsible_Person_Name](#responsible_person_name)|`nvarchar` `ML`|Primary responsible person of the company. NULL means unknown.|
|[Registration_Responsible_Person_Id](#registration_responsible_person_id)|`uniqueidentifier` |The personal record of the primary responsible person as per registration. NULL means unknown|
|[Registration_Responsible_Person_Id_Text](#registration_responsible_person_id_text)|`nvarchar` `ML`|The name of the party|
|[Registration_Primary_Address](#registration_primary_address)|`nvarchar` `ML`|The primary registration address of the company.|
|[Country_Id](#country_id)|`uniqueidentifier` |The country, where the company is registered.|
|[Country_Id_Text](#country_id_text)|`nvarchar` `ML`|Name of the country|
|[City](#city)|`nvarchar` `ML`|The city in which the company is registered.|
|[Person_Id](#person_id)|`uniqueidentifier` `PK`|Unique person Id|
|[Person_First_Name](#person_first_name)|`nvarchar` `ML`||
|[Person_Middle_Name](#person_middle_name)|`nvarchar` `ML`||
|[Person_Last_Name](#person_last_name)|`nvarchar` `ML`||
|[Person_Party_Name](#person_party_name)|`nvarchar` `ML`|The name of the party|
|[Person_Title](#person_title)|`nvarchar` `ML`||
|[Person_Gender](#person_gender)|`nvarchar` Allowed: `F`, `M`||
|[Person_Birth_Date](#person_birth_date)|`datetime` ||
|[Person_Nationality](#person_nationality)|`uniqueidentifier` ||
|[Person_Nationality_Text](#person_nationality_text)|`nvarchar` `ML`||
|[Person_National_Number](#person_national_number)|`nvarchar` ||
|[Person_Passport_Number](#person_passport_number)|`nvarchar` ||
|[Person_Passport_Issuing_Date](#person_passport_issuing_date)|`datetime` ||
|[Person_Notes](#person_notes)|`nvarchar` ||
|[Bank_Code](#bank_code)|`nvarchar` ||
|[Bank_Name](#bank_name)|`nvarchar` `ML`|The full name of the bank|
|[Bank_Branch_Name](#bank_branch_name)|`nvarchar` `ML`|The name of the branch office of the bank, where the account is located. Required (not-null) only for own accounts for printing or exporting bank payments|
|[Bank_Address](#bank_address)|`nvarchar` `ML`|The address of the bank or the bank branch office. Required (not-null) only for own accounts for printing or exporting bank payments|
|[Bank_Account_Code](#bank_account_code)|`nvarchar` |The code of the account, usually the IBAN code|

## Columns

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

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Person_First_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Person_Middle_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Person_Last_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Person_Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Person_Title

| Property | Value |
| - | - |
|Type|nvarchar|

### Person_Gender

| Property | Value |
| - | - |
|Type|nvarchar|

### Person_Birth_Date

| Property | Value |
| - | - |
|Type|datetime|

### Person_Nationality

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Person_Nationality_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Person_National_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Person_Passport_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Person_Passport_Issuing_Date

| Property | Value |
| - | - |
|Type|datetime|

### Person_Notes

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


