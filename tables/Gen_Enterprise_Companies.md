# Table Gen_Enterprise_Companies

The companies in the enterprise that issue documents. Entity: Gen_Enterprise_Companies

## Summary

| Name | Type | Description |
| - | - | --- |
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` `PK`||
|[Company_Id](#company_id)|`uniqueidentifier` |Contains the base company data on which this enterprise company is based.|
|[Base_Currency_Id](#base_currency_id)|`uniqueidentifier` |The base currency for summary reporting for this company.|
|[Default_Language](#default_language)|`nvarchar(10)` Allowed: `bg`, `en`|The default language for multi-language names in the definitions (like Customer_Name, Product_Name, ...).|
|[Default_Costing_Method](#default_costing_method)|`nvarchar(4)` Allowed: `AVG`, `EXP`, `BLD`|Default method for cost evaluation (if not specified in the product). Currently supported: EXP - Explicit lot specifying; AVG - Average cost|
|[Exchange_Difference_Debit_Account_Id](#exchange_difference_debit_account_id)|`uniqueidentifier` |Account for balancing accounting vouchers with debit difference due to currency exchanges|
|[Exchange_Difference_Credit_Account_Id](#exchange_difference_credit_account_id)|`uniqueidentifier` |Account for balancing accounting vouchers with credit difference due to currency exchanges|
|[Advance_Product_Id](#advance_product_id)|`uniqueidentifier` |Product that is used for handling advances in trade documents.|
|[VAT_Document_Amount_Type_Id](#vat_document_amount_type_id)|`uniqueidentifier` |The document amount that is used to determine the amount of the VAT entries when they are generated.|
|[UI_Base_Color](#ui_base_color)|`int` |When not NULL, specifies the background color to use for visualization of the UI when the current enterprise company is selected. The color is in RGBA color format.|
|[BI_Start_Date](#bi_start_date)|`datetime` |Defines the period for which BI extracts data. BI includes documents with "Document Date" greater than or equal to "BI Start Date"|
|[Row_Version](#row_version)|`timestamp` ||
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` ||
|[Edit_Period_Start_Date](#edit_period_start_date)|`datetime` |Start date of the priod when the documents can be edited|
|[Is_Active](#is_active)|`bit` |Indicates whether the current Enterprise company  is active.|
|[Default_Customer_Credit_Limit_Base](#default_customer_credit_limit_base)|`decimal(18, 2)` ||
|[Print_Images_Retention_Months](#print_images_retention_months)|`int` |A period of months for which the printed images of the documents will be kept.|

## Columns

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Base_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Language

| Property | Value |
| - | - |
|Type|nvarchar(10)|

### Default_Costing_Method

| Property | Value |
| - | - |
|Type|nvarchar(4)|

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

### UI_Base_Color

| Property | Value |
| - | - |
|Type|int|

### BI_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Edit_Period_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Default_Customer_Credit_Limit_Base

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Print_Images_Retention_Months

| Property | Value |
| - | - |
|Type|int|


