# Table Crm_Offer_Lines

Detail records (lines) of Offers. Entity: Crm_Offer_Lines

## Owner Tables Hierarchy

* [Crm_Offers](Crm_Offers.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` ||
|[Is_Selected](#is_selected)|`bit` |1 when the line is selected for further processing (ordering), 0 otherwise.|
|[Variant](#variant)|`nvarchar(60)` |Name or number of variant of the whole offer. When multiple lines have the same variant, they are selected for ordering together.|
|[Product_Id](#product_id)|`uniqueidentifier` |The offered product.|
|[Product_Description](#product_description)|`nvarchar(254)` `ML`|The description of the offered product. Initially copied from the name of the offered product.|
|[Quantity](#quantity)|`decimal(12, 3)` |Quantity offered.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Unit_Price](#unit_price)|`decimal(14, 5)` |The unit price of the offered product. It is specified in the measurement unit of Quantity.|
|[Line_Amount](#line_amount)|`decimal(14, 2)` |Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount.|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Guarantee period in days for the offered product. NULL for non-serviced products|
|[Offer_Line_Id](#offer_line_id)|`uniqueidentifier` `PK`||
|[Notes](#notes)|`nvarchar(254)` ||
|[Quantity_Base](#quantity_base)|`decimal(12, 3)` Readonly|The equivalent of Quantity in the base measurement unit of the Product|
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |Not NULL, when the product is selected using a coding system code.|
|[Choice_Group_Name](#choice_group_name)|`nvarchar(60)` |Name of a group of alternative lines, only one of which can be selected for ordering. Lines are grouped based on the exact name of the Choice Group.|
|[Line_Custom_Discount_Percent](#line_custom_discount_percent)|`decimal(7, 6)` |Operator defined discount percentage, specified for this line.|
|[Delivery_Term_Days](#delivery_term_days)|`int` |Delivery term in days. When Required Delivery Date is specified (not NULL), it takes precedence and this is ignored.|
|[Row_Version](#row_version)|`timestamp` ||
|[Line_Standard_Discount_Percent](#line_standard_discount_percent)|`decimal(7, 6)` |The discount percentage, applied through the standard discount policy.|
|[Line_Discount_Id](#line_discount_id)|`uniqueidentifier` |When not NULL, contains the discount policy selected for this line.|
|[Product_Price_Id](#product_price_id)|`uniqueidentifier` |Not NULL when the price has been selected from the list of valid standard prices|
|[Offer_Id](#offer_id)|`uniqueidentifier` ||
|[Required_Delivery_Date](#required_delivery_date)|`date` |Date, when the delivery is required. Alternative to Delivery Term Days. When NULL, Delivery Term Days is used.|
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(12, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

## Columns

### Line_No


Line_No

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
|Autoincrement|10|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Line_No](Crm_Offer_Lines.md#line_no)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Is_Selected


Is_Selected


1 when the line is selected for further processing (ordering), 0 otherwise.


1 when the line is selected for further processing (ordering), 0 otherwise.

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
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Is_Selected](Crm_Offer_Lines.md#is_selected)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Variant


Variant


Name or number of variant of the whole offer. When multiple lines have the same variant, they are selected for ordering together.


Name or number of variant of the whole offer. When multiple lines have the same variant, they are selected for ordering together.

| Property | Value |
| - | - |
|Type|nvarchar(60)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Variant](Crm_Offer_Lines.md#variant)|
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
|Visible|no|
|Max Length|60|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Product_Id


Product_Id


The offered product.


The offered product.

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
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Product_Id](Crm_Offer_Lines.md#product_id)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Product_Description


Product_Description


The description of the offered product. Initially copied from the name of the offered product.


The description of the offered product. Initially copied from the name of the offered product.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Product_Description](Crm_Offer_Lines.md#product_description)|
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
|Max Length|254|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Quantity


Quantity


Quantity offered.


Quantity offered.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Quantity](Crm_Offer_Lines.md#quantity)|
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
|Order|5|
|Summary Type|Sum|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Quantity_Unit_Id


Quantity_Unit_Id


The measurement unit of Quantity.


The measurement unit of Quantity.

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
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Quantity_Unit_Id](Crm_Offer_Lines.md#quantity_unit_id)|
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
|UI Width|Short|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Unit_Price


Unit_Price


The unit price of the offered product. It is specified in the measurement unit of Quantity.


The unit price of the offered product. It is specified in the measurement unit of Quantity.

| Property | Value |
| - | - |
|Type|decimal(14, 5)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Unit_Price](Crm_Offer_Lines.md#unit_price)|
|Format|N4|
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
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Line_Amount


Line_Amount


Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount.


Amount for the line in the currency of the parent document. Usually equals Quantity * Unit_Price. When Quantity = 0, Unit Price is undefined and this contains the total line amount.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Line_Amount](Crm_Offer_Lines.md#line_amount)|
|Format|N2|
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
|Order|8|
|Summary Type|Sum|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Guarantee_Period_Days


Guarantee_Period_Days


Guarantee period in days for the offered product. NULL for non-serviced products


Guarantee period in days for the offered product. NULL for non-serviced products

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
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Guarantee_Period_Days](Crm_Offer_Lines.md#guarantee_period_days)|
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
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Offer_Line_Id


Offer_Line_Id

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
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Offer_Line_Id](Crm_Offer_Lines.md#offer_line_id)|
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

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Notes](Crm_Offer_Lines.md#notes)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Quantity_Base


Quantity_Base


The equivalent of Quantity in the base measurement unit of the Product


The equivalent of Quantity in the base measurement unit of the Product

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Quantity_Base](Crm_Offer_Lines.md#quantity_base)|
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

### Product_Code_Id


Product_Code_Id


Not NULL, when the product is selected using a coding system code.


Not NULL, when the product is selected using a coding system code.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Product_Codes](Gen_Product_Codes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Product_Code_Id](Crm_Offer_Lines.md#product_code_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Choice_Group_Name


Choice_Group_Name


Name of a group of alternative lines, only one of which can be selected for ordering. Lines are grouped based on the exact name of the Choice Group.


Name of a group of alternative lines, only one of which can be selected for ordering. Lines are grouped based on the exact name of the Choice Group.

| Property | Value |
| - | - |
|Type|nvarchar(60)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Choice_Group_Name](Crm_Offer_Lines.md#choice_group_name)|
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
|Visible|no|
|Max Length|60|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Line_Custom_Discount_Percent


Line_Custom_Discount_Percent


Operator defined discount percentage, specified for this line.


Operator defined discount percentage, specified for this line.

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
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Line_Custom_Discount_Percent](Crm_Offer_Lines.md#line_custom_discount_percent)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

### Delivery_Term_Days


Delivery_Term_Days


Delivery term in days. When Required Delivery Date is specified (not NULL), it takes precedence and this is ignored.


Delivery term in days. When Required Delivery Date is specified (not NULL), it takes precedence and this is ignored.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Delivery_Term_Days](Crm_Offer_Lines.md#delivery_term_days)|
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
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Row_Version](Crm_Offer_Lines.md#row_version)|
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

### Line_Standard_Discount_Percent


Line_Standard_Discount_Percent


The discount percentage, applied through the standard discount policy.


The discount percentage, applied through the standard discount policy.

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
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Line_Standard_Discount_Percent](Crm_Offer_Lines.md#line_standard_discount_percent)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

### Line_Discount_Id


Line_Discount_Id


When not NULL, contains the discount policy selected for this line.


When not NULL, contains the discount policy selected for this line.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Line_Discounts](Crm_Line_Discounts.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Line_Discount_Id](Crm_Offer_Lines.md#line_discount_id)|
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
|Equals|NULL|yes|no|

### Product_Price_Id


Product_Price_Id


Not NULL when the price has been selected from the list of valid standard prices


Not NULL when the price has been selected from the list of valid standard prices

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Product_Prices](Crm_Product_Prices.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Product_Price_Id](Crm_Offer_Lines.md#product_price_id)|
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
|Equals|NULL|yes|no|

### Offer_Id


Offer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Crm_Offers](Crm_Offers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Offer_Id](Crm_Offer_Lines.md#offer_id)|
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

### Required_Delivery_Date


Required_Delivery_Date


Date, when the delivery is required. Alternative to Delivery Term Days. When NULL, Delivery Term Days is used.


Date, when the delivery is required. Alternative to Delivery Term Days. When NULL, Delivery Term Days is used.

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
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Required_Delivery_Date](Crm_Offer_Lines.md#required_delivery_date)|
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
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Standard_Quantity_Base


Standard_Quantity_Base


The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.


The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Offer_Lines](Crm_Offer_Lines.md).[Standard_Quantity_Base](Crm_Offer_Lines.md#standard_quantity_base)|
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


