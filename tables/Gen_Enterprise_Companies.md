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


Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Enterprise_Company_Id](Gen_Enterprise_Companies.md#enterprise_company_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Company_Id


Company_Id


Contains the base company data on which this enterprise company is based.


Contains the base company data on which this enterprise company is based.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Companies](Cm_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Company_Id](Gen_Enterprise_Companies.md#company_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Base_Currency_Id


Base_Currency_Id


The base currency for summary reporting for this company.


The base currency for summary reporting for this company.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Currencies](Gen_Currencies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Base_Currency_Id](Gen_Enterprise_Companies.md#base_currency_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Default_Language


Default_Language


The default language for multi-language names in the definitions (like Customer_Name, Product_Name, ...).


The default language for multi-language names in the definitions (like Customer_Name, Product_Name, ...).

| Property | Value |
| - | - |
|Type|nvarchar(10)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`bg`, `en`|
|Default Value|en|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Default_Language](Gen_Enterprise_Companies.md#default_language)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|10|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Default_Costing_Method


Default_Costing_Method


Default method for cost evaluation (if not specified in the product). Currently supported: EXP - Explicit lot specifying; AVG - Average cost


Default method for cost evaluation (if not specified in the product). Currently supported: EXP - Explicit lot specifying; AVG - Average cost

| Property | Value |
| - | - |
|Type|nvarchar(4)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`AVG`, `EXP`, `BLD`|
|Default Value|AVG|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Default_Costing_Method](Gen_Enterprise_Companies.md#default_costing_method)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|4|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Exchange_Difference_Debit_Account_Id


Exchange_Difference_Debit_Account_Id


Account for balancing accounting vouchers with debit difference due to currency exchanges


Account for balancing accounting vouchers with debit difference due to currency exchanges

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Acc_Accounts](Acc_Accounts.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Exchange_Difference_Debit_Account_Id](Gen_Enterprise_Companies.md#exchange_difference_debit_account_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Exchange_Difference_Credit_Account_Id


Exchange_Difference_Credit_Account_Id


Account for balancing accounting vouchers with credit difference due to currency exchanges


Account for balancing accounting vouchers with credit difference due to currency exchanges

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Acc_Accounts](Acc_Accounts.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Exchange_Difference_Credit_Account_Id](Gen_Enterprise_Companies.md#exchange_difference_credit_account_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Advance_Product_Id


Advance_Product_Id


Product that is used for handling advances in trade documents.


Product that is used for handling advances in trade documents.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Advance_Product_Id](Gen_Enterprise_Companies.md#advance_product_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### VAT_Document_Amount_Type_Id


VAT_Document_Amount_Type_Id


The document amount that is used to determine the amount of the VAT entries when they are generated.


The document amount that is used to determine the amount of the VAT entries when they are generated.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[VAT_Document_Amount_Type_Id](Gen_Enterprise_Companies.md#vat_document_amount_type_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### UI_Base_Color


UI_Base_Color


When not NULL, specifies the background color to use for visualization of the UI when the current enterprise company is selected. The color is in RGBA color format.


When not NULL, specifies the background color to use for visualization of the UI when the current enterprise company is selected. The color is in RGBA color format.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[UI_Base_Color](Gen_Enterprise_Companies.md#ui_base_color)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### BI_Start_Date


BI_Start_Date


Defines the period for which BI extracts data. BI includes documents with "Document Date" greater than or equal to "BI Start Date"


Defines the period for which BI extracts data. BI includes documents with "Document Date" greater than or equal to "BI Start Date"

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[BI_Start_Date](Gen_Enterprise_Companies.md#bi_start_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Row_Version](Gen_Enterprise_Companies.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Access_Key_Id


Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Access_Keys](Sec_Access_Keys.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Access_Key_Id](Gen_Enterprise_Companies.md#access_key_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Edit_Period_Start_Date


Edit_Period_Start_Date


Start date of the priod when the documents can be edited


Start date of the priod when the documents can be edited

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Edit_Period_Start_Date](Gen_Enterprise_Companies.md#edit_period_start_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Active


Is_Active


Indicates whether the current Enterprise company  is active.


Indicates whether the current Enterprise company  is active.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Is_Active](Gen_Enterprise_Companies.md#is_active)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Default_Customer_Credit_Limit_Base


Default_Customer_Credit_Limit_Base

| Property | Value |
| - | - |
|Type|decimal(18, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Default_Customer_Credit_Limit_Base](Gen_Enterprise_Companies.md#default_customer_credit_limit_base)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Print_Images_Retention_Months


Print_Images_Retention_Months


A period of months for which the printed images of the documents will be kept.


A period of months for which the printed images of the documents will be kept.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|60|
|Derived From|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md).[Print_Images_Retention_Months](Gen_Enterprise_Companies.md#print_images_retention_months)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|GreaterThanOrLessThan|None|no|no|


