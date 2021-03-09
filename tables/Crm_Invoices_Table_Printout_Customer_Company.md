# Procedure Crm_Invoices_Table_Printout_Customer_Company


## Summary

| Name | Type | Description |
| - | - | --- |
|[Company_Id](#company_id)|`uniqueidentifier` ||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Party_Id_Text](#party_id_text)|`nvarchar` `ML`|The name of the party|
|[Registration_Type](#registration_type)|`nvarchar` ||
|[Registration_Number](#registration_number)|`nvarchar` ||
|[Registration_VAT_Number](#registration_vat_number)|`nvarchar` ||
|[Responsible_Person_Name](#responsible_person_name)|`nvarchar` ||
|[Registration_Responsible_Person_Id](#registration_responsible_person_id)|`uniqueidentifier` ||
|[Registration_Responsible_Person_Id_Text](#registration_responsible_person_id_text)|`nvarchar` ||
|[Registration_Primary_Address](#registration_primary_address)|`nvarchar` ||
|[Country_Id](#country_id)|`uniqueidentifier` ||
|[Country_Id_Text](#country_id_text)|`nvarchar` `ML`|Name of the country|
|[City](#city)|`nvarchar` ||
|[Person_Id](#person_id)|`uniqueidentifier` `PK`|Unique person Id|
|[Person_First_Name](#person_first_name)|`nvarchar` `ML`|First name of the person.|
|[Person_Middle_Name](#person_middle_name)|`nvarchar` `ML`|Middle name of the person.|
|[Person_Last_Name](#person_last_name)|`nvarchar` `ML`|Last name of the person.|
|[Person_Party_Name](#person_party_name)|`nvarchar` ||
|[Person_Title](#person_title)|`nvarchar` `ML`|The persons title. It may be one of the standard titles - Mr., Mrs., etc., but it can also contains professional or academic qualification.|
|[Person_Gender](#person_gender)|`nvarchar` Allowed: `F`, `M`|Person gender. M=Male;F=Female;NULL=not known/not provided|
|[Person_Birth_Date](#person_birth_date)|`datetime` |Birth date. NULL means unknown|
|[Person_Nationality](#person_nationality)|`uniqueidentifier` |Person's nationality. NULL means the default (same as enterprise) nationality|
|[Person_Nationality_Text](#person_nationality_text)|`nvarchar` `ML`||
|[Person_National_Number](#person_national_number)|`nvarchar` |Government assigned unique personal number. NULL means unknown|
|[Person_Passport_Number](#person_passport_number)|`nvarchar` |Current passport number. NULL means unknown|
|[Person_Passport_Issuing_Date](#person_passport_issuing_date)|`datetime` |Date of issuing the passport. NULL means unknown|
|[Person_Notes](#person_notes)|`nvarchar` |Internal notes for the person|
|[Bank_Code](#bank_code)|`nvarchar` ||
|[Bank_Name](#bank_name)|`nvarchar` ||
|[Bank_Branch_Name](#bank_branch_name)|`nvarchar` ||
|[Bank_Address](#bank_address)|`nvarchar` ||
|[Bank_Account_Code](#bank_account_code)|`nvarchar` ||

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


