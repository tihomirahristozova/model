# Query Nat_BG_VAT_Declarations_Table_Purchases_Ledger_2007_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[VAT_Declaration_Id](#vat_declaration_id)|`uniqueidentifier` `PK`|Unique identification of the VAT declaration.|
|[Enterprise_Company_Registration_VAT_Number](#enterprise_company_registration_vat_number)|`nvarchar` |VAT registration number where applicable. NULL means that VAT number is not applicable or unknown|
|[VAT_Period](#vat_period)|`nvarchar` ||
|[Enterprise_Company_Branch](#enterprise_company_branch)|`int` ||
|[Line_No](#line_no)|`int` ||
|[VAT_Code](#vat_code)|`nvarchar` ||
|[Document_No](#document_no)|`nvarchar` |Document number, unique within Document_Type_Id|
|[Document_Date](#document_date)|`date` |The date on which the document was issued|
|[Column8a_Data](#column8a_data)|`nvarchar` ||
|[Party_Registration_VAT_Number](#party_registration_vat_number)|`nvarchar` |VAT number by registration (or national number) for the party specified by Party_Id.|
|[Party_Name](#party_name)|`nvarchar` `ML`|The name of the party|
|[Notes](#notes)|`nvarchar` ||
|[Base_Amount_Without_Tax_Credit](#base_amount_without_tax_credit)|`decimal(0, 0)` ||
|[Base_Amount_With_Full_Tax_Credit](#base_amount_with_full_tax_credit)|`decimal(0, 0)` ||
|[VAT_Amount_With_Full_Tax_Credit](#vat_amount_with_full_tax_credit)|`decimal(0, 0)` ||
|[Base_Amount_With_Partial_Tax_Credit](#base_amount_with_partial_tax_credit)|`decimal(0, 0)` ||
|[VAT_Amount_With_Partial_Tax_Credit](#vat_amount_with_partial_tax_credit)|`decimal(0, 0)` ||
|[Annual_Correction](#annual_correction)|`decimal(0, 0)` ||
|[Base_Amount_Third_Party_Operation](#base_amount_third_party_operation)|`decimal(0, 0)` ||

## Columns

### VAT_Declaration_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Registration_VAT_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### VAT_Period

| Property | Value |
| - | - |
|Type|nvarchar|

### Enterprise_Company_Branch

| Property | Value |
| - | - |
|Type|int|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### VAT_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### Column8a_Data

| Property | Value |
| - | - |
|Type|nvarchar|

### Party_Registration_VAT_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Base_Amount_Without_Tax_Credit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Base_Amount_With_Full_Tax_Credit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### VAT_Amount_With_Full_Tax_Credit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Base_Amount_With_Partial_Tax_Credit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### VAT_Amount_With_Partial_Tax_Credit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Annual_Correction

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Base_Amount_Third_Party_Operation

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


