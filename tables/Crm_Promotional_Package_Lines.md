# Table Crm_Promotional_Package_Lines

Detail records (lines) of promotional package definition. Entity: Crm_Promotional_Package_Lines

## Owner Tables Hierarchy

* [Crm_Promotional_Packages](Crm_Promotional_Packages.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Promotional_Package_Line_Id](#promotional_package_line_id)|`uniqueidentifier` `PK`||
|[Promotional_Package_Id](#promotional_package_id)|`uniqueidentifier` ||
|[Line_Number](#line_number)|`int` |Consecutive line number|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which is included in the promotional package|
|[Quantity](#quantity)|`decimal(9, 3)` |The quantity of the product in the package in the base measurement unit of the Product.|
|[Standard_Discount_Percent_Adjust](#standard_discount_percent_adjust)|`decimal(7, 6)` |The value of change (in percents) for the standard discount|
|[Standard_Discount_Adjust_Or_Replace](#standard_discount_adjust_or_replace)|`nvarchar(1)` Allowed: `A`, `R`, `M`|Specifies standard discount change action: A=ADD, M=Mark down - apply after standard discount; R=REPLACE the standard discount|
|[Unit_Price](#unit_price)|`decimal(13, 5)` |When not null specifies directly unit price for the product. When NULL, the package specifies only discount|
|[Unit_Price_Currency_Id](#unit_price_currency_id)|`uniqueidentifier` |Currency of the unit price. NULL if the package specifies only discount|
|[Row_Version](#row_version)|`timestamp` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` |The Product lot number in the promotional package.|

## Columns

### Promotional_Package_Line_Id


Promotional_Package_Line_Id

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
|Derived From|[Crm_Promotional_Package_Lines](Crm_Promotional_Package_Lines.md).[Promotional_Package_Line_Id](Crm_Promotional_Package_Lines.md#promotional_package_line_id)|
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

### Promotional_Package_Id


Promotional_Package_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Crm_Promotional_Packages](Crm_Promotional_Packages.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Package_Lines](Crm_Promotional_Package_Lines.md).[Promotional_Package_Id](Crm_Promotional_Package_Lines.md#promotional_package_id)|
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

### Line_Number


Line_Number


Consecutive line number


Consecutive line number

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
|Derived From|[Crm_Promotional_Package_Lines](Crm_Promotional_Package_Lines.md).[Line_Number](Crm_Promotional_Package_Lines.md#line_number)|
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

### Product_Id


Product_Id


The product, which is included in the promotional package


The product, which is included in the promotional package

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
|Derived From|[Crm_Promotional_Package_Lines](Crm_Promotional_Package_Lines.md).[Product_Id](Crm_Promotional_Package_Lines.md#product_id)|
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


The quantity of the product in the package in the base measurement unit of the Product.


The quantity of the product in the package in the base measurement unit of the Product.

| Property | Value |
| - | - |
|Type|decimal(9, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Crm_Promotional_Package_Lines](Crm_Promotional_Package_Lines.md).[Quantity](Crm_Promotional_Package_Lines.md#quantity)|
|Format|N3|
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
|GreaterThanOrLessThan|None|yes|no|

### Standard_Discount_Percent_Adjust


Standard_Discount_Percent_Adjust


The value of change (in percents) for the standard discount


The value of change (in percents) for the standard discount

| Property | Value |
| - | - |
|Type|decimal(7, 6)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsPercent|
|Default Value|0|
|Derived From|[Crm_Promotional_Package_Lines](Crm_Promotional_Package_Lines.md).[Standard_Discount_Percent_Adjust](Crm_Promotional_Package_Lines.md#standard_discount_percent_adjust)|
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

### Standard_Discount_Adjust_Or_Replace


Standard_Discount_Adjust_Or_Replace


Specifies standard discount change action: A=ADD, M=Mark down - apply after standard discount; R=REPLACE the standard discount


Specifies standard discount change action: A=ADD, M=Mark down - apply after standard discount; R=REPLACE the standard discount

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`A`, `R`, `M`|
|Default Value|R|
|Derived From|[Crm_Promotional_Package_Lines](Crm_Promotional_Package_Lines.md).[Standard_Discount_Adjust_Or_Replace](Crm_Promotional_Package_Lines.md#standard_discount_adjust_or_replace)|
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
|Max Length|1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Unit_Price


Unit_Price


When not null specifies directly unit price for the product. When NULL, the package specifies only discount


When not null specifies directly unit price for the product. When NULL, the package specifies only discount

| Property | Value |
| - | - |
|Type|decimal(13, 5)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Package_Lines](Crm_Promotional_Package_Lines.md).[Unit_Price](Crm_Promotional_Package_Lines.md#unit_price)|
|Format|N2|
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

### Unit_Price_Currency_Id


Unit_Price_Currency_Id


Currency of the unit price. NULL if the package specifies only discount


Currency of the unit price. NULL if the package specifies only discount

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
|Derived From|[Crm_Promotional_Package_Lines](Crm_Promotional_Package_Lines.md).[Unit_Price_Currency_Id](Crm_Promotional_Package_Lines.md#unit_price_currency_id)|
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
|Derived From|[Crm_Promotional_Package_Lines](Crm_Promotional_Package_Lines.md).[Row_Version](Crm_Promotional_Package_Lines.md#row_version)|
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

### Lot_Id


Lot_Id


The Product lot number in the promotional package.


The Product lot number in the promotional package.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Lots](Inv_Lots.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Package_Lines](Crm_Promotional_Package_Lines.md).[Lot_Id](Crm_Promotional_Package_Lines.md#lot_id)|
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


