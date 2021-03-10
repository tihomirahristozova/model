# Table Crm_Sales_Person_Target_Lines

Detail records (lines) of targets for sales persons. Entity: Crm_Sales_Person_Target_Lines

## Owner Tables Hierarchy

* [Crm_Sales_Person_Targets](Crm_Sales_Person_Targets.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sales_Person_Target_Line_Id](#sales_person_target_line_id)|`uniqueidentifier` `PK`||
|[Sales_Person_Target_Id](#sales_person_target_id)|`uniqueidentifier` ||
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` |Sales person to whom the target is assigned|
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` |Product group for which the target is defined|
|[Period_Month](#period_month)|`tinyint` |Month of the period in which the target must be fulfilled (the period is determined by specifying a month and an year)|
|[Period_Year](#period_year)|`smallint` |Year of the period in which the target must be fulfilled (the period is determined by specifying a month and an year)|
|[Target_Amount](#target_amount)|`decimal(18, 2)` |Target amount to be fulfilled by the specified sales person. Deprecated - use Target_Value|
|[Target_Amount_Currency_Id](#target_amount_currency_id)|`uniqueidentifier` |Deprecated - use currency in document header|
|[Period_Date](#period_date)|`datetime` Readonly|Calculated date representation of the target period (used for grouping, filtering and other auxiliary purposes)|
|[Target_Type](#target_type)|`nvarchar(5)` Allowed: `SALES`, `BONUS`, `PROMO`, `LOCNT`|Type of target. Defines the meaning of Target_Value. SALES-sales amount, BONUS-count of bonus progs, PACK-count of promo packs|
|[Target_Value](#target_value)|`decimal(9, 2)` |Value of target. Meaning depends on target type|
|[Target_Weight](#target_weight)|`decimal(5, 2)` |Relative weight of target, comparatively to other targets|
|[Bonus_Program_Id](#bonus_program_id)|`uniqueidentifier` |Bonus program Id when the target type is BONUS, NULL otherwise|
|[Promotional_Package_Id](#promotional_package_id)|`uniqueidentifier` |Promotional Package Id when the target type is PROMO, NULL otherwise|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sales_Person_Target_Line_Id


Sales_Person_Target_Line_Id

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
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Sales_Person_Target_Line_Id](Crm_Sales_Person_Target_Lines.md#sales_person_target_line_id)|
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
|Equals|NULL|no|yes|

### Sales_Person_Target_Id


Sales_Person_Target_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Crm_Sales_Person_Targets](Crm_Sales_Person_Targets.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Sales_Person_Target_Id](Crm_Sales_Person_Target_Lines.md#sales_person_target_id)|
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
|Equals|NULL|no|no|

### Sales_Person_Id


Sales_Person_Id


Sales person to whom the target is assigned


Sales person to whom the target is assigned

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Sales_Persons](Crm_Sales_Persons.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Sales_Person_Id](Crm_Sales_Person_Target_Lines.md#sales_person_id)|
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

### Product_Group_Id


Product_Group_Id


Product group for which the target is defined


Product group for which the target is defined

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Product_Groups](Gen_Product_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Product_Group_Id](Crm_Sales_Person_Target_Lines.md#product_group_id)|
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
|Equals|NULL|yes|no|

### Period_Month


Period_Month


Month of the period in which the target must be fulfilled (the period is determined by specifying a month and an year)


Month of the period in which the target must be fulfilled (the period is determined by specifying a month and an year)

| Property | Value |
| - | - |
|Type|tinyint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Period_Month](Crm_Sales_Person_Target_Lines.md#period_month)|
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
|GreaterThanOrLessThan|None|no|no|

### Period_Year


Period_Year


Year of the period in which the target must be fulfilled (the period is determined by specifying a month and an year)


Year of the period in which the target must be fulfilled (the period is determined by specifying a month and an year)

| Property | Value |
| - | - |
|Type|smallint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Period_Year](Crm_Sales_Person_Target_Lines.md#period_year)|
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
|GreaterThanOrLessThan|None|no|no|

### Target_Amount


Target_Amount


Target amount to be fulfilled by the specified sales person. Deprecated - use Target_Value


Target amount to be fulfilled by the specified sales person. Deprecated - use Target_Value

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
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Target_Amount](Crm_Sales_Person_Target_Lines.md#target_amount)|
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

### Target_Amount_Currency_Id


Target_Amount_Currency_Id


Deprecated - use currency in document header


Deprecated - use currency in document header

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Currencies](Gen_Currencies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Target_Amount_Currency_Id](Crm_Sales_Person_Target_Lines.md#target_amount_currency_id)|
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
|Equals|NULL|yes|no|

### Period_Date


Period_Date


Calculated date representation of the target period (used for grouping, filtering and other auxiliary purposes)


Calculated date representation of the target period (used for grouping, filtering and other auxiliary purposes)

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Period_Date](Crm_Sales_Person_Target_Lines.md#period_date)|
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

### Target_Type


Target_Type


Type of target. Defines the meaning of Target_Value. SALES-sales amount, BONUS-count of bonus progs, PACK-count of promo packs


Type of target. Defines the meaning of Target_Value. SALES-sales amount, BONUS-count of bonus progs, PACK-count of promo packs

| Property | Value |
| - | - |
|Type|nvarchar(5)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`SALES`, `BONUS`, `PROMO`, `LOCNT`|
|Default Value|SALES|
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Target_Type](Crm_Sales_Person_Target_Lines.md#target_type)|
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
|Max Length|5|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Target_Value


Target_Value


Value of target. Meaning depends on target type


Value of target. Meaning depends on target type

| Property | Value |
| - | - |
|Type|decimal(9, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Target_Value](Crm_Sales_Person_Target_Lines.md#target_value)|
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

### Target_Weight


Target_Weight


Relative weight of target, comparatively to other targets


Relative weight of target, comparatively to other targets

| Property | Value |
| - | - |
|Type|decimal(5, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Target_Weight](Crm_Sales_Person_Target_Lines.md#target_weight)|
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

### Bonus_Program_Id


Bonus_Program_Id


Bonus program Id when the target type is BONUS, NULL otherwise


Bonus program Id when the target type is BONUS, NULL otherwise

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Bonus_Programs](Crm_Bonus_Programs.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Bonus_Program_Id](Crm_Sales_Person_Target_Lines.md#bonus_program_id)|
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
|Equals|NULL|yes|no|

### Promotional_Package_Id


Promotional_Package_Id


Promotional Package Id when the target type is PROMO, NULL otherwise


Promotional Package Id when the target type is PROMO, NULL otherwise

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Promotional_Packages](Crm_Promotional_Packages.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Promotional_Package_Id](Crm_Sales_Person_Target_Lines.md#promotional_package_id)|
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
|Derived From|[Crm_Sales_Person_Target_Lines](Crm_Sales_Person_Target_Lines.md).[Row_Version](Crm_Sales_Person_Target_Lines.md#row_version)|
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


