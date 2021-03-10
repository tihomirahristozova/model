# Table Log_Logistic_Unit_Contents

Theoretical or actual content of a logistic unit. Entity: Log_Logistic_Unit_Contents (Introduced in version 21.1.0.77)

## Owner Tables Hierarchy

* [Log_Logistic_Units](Log_Logistic_Units.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Logistic_Unit_Content_Id](#logistic_unit_content_id)|`uniqueidentifier` `PK`||
|[Logistic_Unit_Id](#logistic_unit_id)|`uniqueidentifier` |The containing logistic unit.|
|[Line_No](#line_no)|`int` |Consecutive position within the logistic unit.|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which is contained in the logistic unit.|
|[Quantity](#quantity)|`decimal(12, 3)` |Quantity of the product in the logistic unit. Expressed in the specified measurement unit.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of the quantity.|
|[Standard_Quantity](#standard_quantity)|`decimal(12, 3)` |The quantity, expessed in the standard measurement unit of the product.|
|[Base_Quantity](#base_quantity)|`decimal(12, 3)` |The quantity, expressed in the base measurement category of the product.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Gross_Weight](#gross_weight)|`decimal(12, 3)` |Gross weight in kilograms (kg). NULL means unknown.|
|[Lot_Number](#lot_number)|`nvarchar(32)` |The production lot number. NULL means unknown.|
|[Expiration_Date](#expiration_date)|`date` |Expiration date of the goods. NULL means unknown or N/A.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Logistic_Unit_Content_Id


Logistic_Unit_Content_Id

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
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Logistic_Unit_Content_Id](Log_Logistic_Unit_Contents.md#logistic_unit_content_id)|
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

### Logistic_Unit_Id


Logistic_Unit_Id


The containing logistic unit.


The containing logistic unit.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Log_Logistic_Units](Log_Logistic_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Logistic_Unit_Id](Log_Logistic_Unit_Contents.md#logistic_unit_id)|
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

### Line_No


Line_No


Consecutive position within the logistic unit.


Consecutive position within the logistic unit.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|1|
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Line_No](Log_Logistic_Unit_Contents.md#line_no)|
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

### Product_Id


Product_Id


The product, which is contained in the logistic unit.


The product, which is contained in the logistic unit.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Product_Id](Log_Logistic_Unit_Contents.md#product_id)|
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

### Quantity


Quantity


Quantity of the product in the logistic unit. Expressed in the specified measurement unit.


Quantity of the product in the logistic unit. Expressed in the specified measurement unit.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Quantity](Log_Logistic_Unit_Contents.md#quantity)|
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

### Quantity_Unit_Id


Quantity_Unit_Id


The measurement unit of the quantity.


The measurement unit of the quantity.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Quantity_Unit_Id](Log_Logistic_Unit_Contents.md#quantity_unit_id)|
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

### Standard_Quantity


Standard_Quantity


The quantity, expessed in the standard measurement unit of the product.


The quantity, expessed in the standard measurement unit of the product.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Standard_Quantity](Log_Logistic_Unit_Contents.md#standard_quantity)|
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
|Equals|NULL|no|no|
|GreaterThanOrLessThan|None|no|no|

### Base_Quantity


Base_Quantity


The quantity, expressed in the base measurement category of the product.


The quantity, expressed in the base measurement category of the product.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Base_Quantity](Log_Logistic_Unit_Contents.md#base_quantity)|
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
|Equals|NULL|no|no|
|GreaterThanOrLessThan|None|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Notes](Log_Logistic_Unit_Contents.md#notes)|
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
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Gross_Weight


Gross_Weight


Gross weight in kilograms (kg). NULL means unknown.


Gross weight in kilograms (kg). NULL means unknown.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Gross_Weight](Log_Logistic_Unit_Contents.md#gross_weight)|
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
|GreaterThanOrLessThan|None|no|no|

### Lot_Number


Lot_Number


The production lot number. NULL means unknown.


The production lot number. NULL means unknown.

| Property | Value |
| - | - |
|Type|nvarchar(32)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Lot_Number](Log_Logistic_Unit_Contents.md#lot_number)|
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
|Max Length|32|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Expiration_Date


Expiration_Date


Expiration date of the goods. NULL means unknown or N/A.


Expiration date of the goods. NULL means unknown or N/A.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Expiration_Date](Log_Logistic_Unit_Contents.md#expiration_date)|
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
|GreaterThanOrLessThan|None|yes|no|

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
|Derived From|[Log_Logistic_Unit_Contents](Log_Logistic_Unit_Contents.md).[Row_Version](Log_Logistic_Unit_Contents.md#row_version)|
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


