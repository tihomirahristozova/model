# Query Nat_BG_VAT_Declarations_Table_VIES_Declaration_2007_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[VAT_Declaration_Id](#vat_declaration_id)|`uniqueidentifier` `PK`|Unique identification of the VAT declaration.|
|[Enterprise_Company_Address](#enterprise_company_address)|`nvarchar` `ML`|The primary registration address of the company.|
|[Declaring_Person_National_Number](#declaring_person_national_number)|`nvarchar` |Government assigned unique personal number. NULL means unknown|
|[Enterprise_Company_Registration_VAT_Number](#enterprise_company_registration_vat_number)|`nvarchar` |VAT registration number where applicable. NULL means that VAT number is not applicable or unknown|
|[VIES_Declaration_Total_Amounts_Section_Code](#vies_declaration_total_amounts_section_code)|`nvarchar` ||
|[Enterprise_Company_Party_Name](#enterprise_company_party_name)|`nvarchar` `ML`|The name of the party|
|[VIES_Declaration_Registered_Company_Section_Code](#vies_declaration_registered_company_section_code)|`nvarchar` ||
|[Declaring_Person_Position](#declaring_person_position)|`nvarchar` |Position of the declaring person in the enterprise company.|
|[Declarer_Type](#declarer_type)|`nvarchar` Allowed: `A`, `R`|Type of the declaring person. A=Attorney, R=Representative.|
|[Declaring_Person_Address](#declaring_person_address)|`nvarchar` |Address for correspondation of the declaring person.|
|[Declaring_Person_Postcode](#declaring_person_postcode)|`nvarchar` |Postcode from the address for correspondation of the declaring person.|
|[Declaring_Person_City](#declaring_person_city)|`nvarchar` |City from the address for correspondation of the declaring person.|
|[Declaring_Person_Full_Name](#declaring_person_full_name)|`nvarchar` `ML`|The name of the party|
|[VIES_Declaration_Declaring_Person_Section_Code](#vies_declaration_declaring_person_section_code)|`nvarchar` ||
|[VIES_Declaration_Lines_Count](#vies_declaration_lines_count)|`int` ||
|[Report_Period](#report_period)|`nvarchar` ||
|[VIES_Declaration_Main_Section_Code](#vies_declaration_main_section_code)|`nvarchar` ||
|[Total_Base_Amount](#total_base_amount)|`decimal(0, 0)` ||
|[Total_Base_Amount_EUSale](#total_base_amount_eusale)|`decimal(0, 0)` ||

## Columns

### VAT_Declaration_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Address

| Property | Value |
| - | - |
|Type|nvarchar|

### Declaring_Person_National_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Enterprise_Company_Registration_VAT_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### VIES_Declaration_Total_Amounts_Section_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Enterprise_Company_Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### VIES_Declaration_Registered_Company_Section_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Declaring_Person_Position

| Property | Value |
| - | - |
|Type|nvarchar|

### Declarer_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Declaring_Person_Address

| Property | Value |
| - | - |
|Type|nvarchar|

### Declaring_Person_Postcode

| Property | Value |
| - | - |
|Type|nvarchar|

### Declaring_Person_City

| Property | Value |
| - | - |
|Type|nvarchar|

### Declaring_Person_Full_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### VIES_Declaration_Declaring_Person_Section_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### VIES_Declaration_Lines_Count

| Property | Value |
| - | - |
|Type|int|

### Report_Period

| Property | Value |
| - | - |
|Type|nvarchar|

### VIES_Declaration_Main_Section_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Total_Base_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Total_Base_Amount_EUSale

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


