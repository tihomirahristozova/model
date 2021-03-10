# Table Scm_Purchase_Order_Lines

Contains detail lines of purchase orders. Entity: Scm_Purchase_Order_Lines

## Owner Tables Hierarchy

* [Scm_Purchase_Orders](Scm_Purchase_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Order_Line_Id](#purchase_order_line_id)|`uniqueidentifier` `PK`||
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` ||
|[Product_Id](#product_id)|`uniqueidentifier` |The ordered product.|
|[Product_Description](#product_description)|`nvarchar(254)` `ML`|The name of the ordered product, initially copied from the name in the product definition. The field can be edited by the user.|
|[Quantity](#quantity)|`decimal(18, 3)` |The quantity ordered.|
|[Confirmed_Quantity](#confirmed_quantity)|`decimal(18, 3)` |The quantity that is confirmed by the supplier. NULL if there was no order confirmation.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Price_Per_Unit](#price_per_unit)|`decimal(14, 5)` |The expected unit price of the ordered products, in the document currency.|
|[Confirmed_Price_Per_Unit](#confirmed_price_per_unit)|`decimal(14, 5)` |The unit price that is confirmed by the supplier. NULL if there was no order confirmation.|
|[Planned_Delivery_Date](#planned_delivery_date)|`datetime` |The planned delivery date for this line.|
|[Purchase_Product_Price_Id](#purchase_product_price_id)|`uniqueidentifier` |When not NULL, specifies that the purchase unit price is loaded automatically from the specified purchase price record.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |When not NULL, specifies that the product was selected using the specified product code record.|
|[Requisition_Line_Id](#requisition_line_id)|`uniqueidentifier` |When not NULL, specifies that the current line is based on the specified requisition line.|
|[Quantity_Base](#quantity_base)|`decimal(18, 3)` Readonly|The equivalence of Quantity, in the base measurement category of the product.|
|[Confirmed_Quantity_Base](#confirmed_quantity_base)|`decimal(18, 3)` Readonly|The theoretical equivalence of Confirmed Quantity in base measurement unit according to the current measurement dimensions of the product.|
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |When not null, indicates that a specific lot is required to be delivered.|
|[Row_Version](#row_version)|`timestamp` ||
|[Parent_Line_No](#parent_line_no)|`int` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` ||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|
|[Confirmed_Standard_Quantity_Base](#confirmed_standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Confirmed Quantity using the measurement ratios.|

## Columns

### Purchase_Order_Line_Id


Purchase_Order_Line_Id

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
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Purchase_Order_Line_Id](Scm_Purchase_Order_Lines.md#purchase_order_line_id)|
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

### Purchase_Order_Id


Purchase_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Scm_Purchase_Orders](Scm_Purchase_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Purchase_Order_Id](Scm_Purchase_Order_Lines.md#purchase_order_id)|
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
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Line_No](Scm_Purchase_Order_Lines.md#line_no)|
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

### Product_Id


Product_Id


The ordered product.


The ordered product.

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
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Product_Id](Scm_Purchase_Order_Lines.md#product_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Product_Description


Product_Description


The name of the ordered product, initially copied from the name in the product definition. The field can be edited by the user.


The name of the ordered product, initially copied from the name in the product definition. The field can be edited by the user.

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
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Product_Description](Scm_Purchase_Order_Lines.md#product_description)|
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
|Order|2147483647|
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


The quantity ordered.


The quantity ordered.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Quantity](Scm_Purchase_Order_Lines.md#quantity)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Confirmed_Quantity


Confirmed_Quantity


The quantity that is confirmed by the supplier. NULL if there was no order confirmation.


The quantity that is confirmed by the supplier. NULL if there was no order confirmation.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Confirmed_Quantity](Scm_Purchase_Order_Lines.md#confirmed_quantity)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

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
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Quantity_Unit_Id](Scm_Purchase_Order_Lines.md#quantity_unit_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Price_Per_Unit


Price_Per_Unit


The expected unit price of the ordered products, in the document currency.


The expected unit price of the ordered products, in the document currency.

| Property | Value |
| - | - |
|Type|decimal(14, 5)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Price_Per_Unit](Scm_Purchase_Order_Lines.md#price_per_unit)|
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

### Confirmed_Price_Per_Unit


Confirmed_Price_Per_Unit


The unit price that is confirmed by the supplier. NULL if there was no order confirmation.


The unit price that is confirmed by the supplier. NULL if there was no order confirmation.

| Property | Value |
| - | - |
|Type|decimal(14, 5)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Confirmed_Price_Per_Unit](Scm_Purchase_Order_Lines.md#confirmed_price_per_unit)|
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

### Planned_Delivery_Date


Planned_Delivery_Date


The planned delivery date for this line.


The planned delivery date for this line.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Planned_Delivery_Date](Scm_Purchase_Order_Lines.md#planned_delivery_date)|
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
|GreaterThanOrLessThan|None|yes|no|

### Purchase_Product_Price_Id


Purchase_Product_Price_Id


When not NULL, specifies that the purchase unit price is loaded automatically from the specified purchase price record.


When not NULL, specifies that the purchase unit price is loaded automatically from the specified purchase price record.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Purchase_Product_Prices](Scm_Purchase_Product_Prices.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Purchase_Product_Price_Id](Scm_Purchase_Order_Lines.md#purchase_product_price_id)|
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
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Notes](Scm_Purchase_Order_Lines.md#notes)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Product_Code_Id


Product_Code_Id


When not NULL, specifies that the product was selected using the specified product code record.


When not NULL, specifies that the product was selected using the specified product code record.

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
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Product_Code_Id](Scm_Purchase_Order_Lines.md#product_code_id)|
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

### Requisition_Line_Id


Requisition_Line_Id


When not NULL, specifies that the current line is based on the specified requisition line.


When not NULL, specifies that the current line is based on the specified requisition line.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Requisition_Lines](Scm_Requisition_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Requisition_Line_Id](Scm_Purchase_Order_Lines.md#requisition_line_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Quantity_Base


Quantity_Base


The equivalence of Quantity, in the base measurement category of the product.


The equivalence of Quantity, in the base measurement category of the product.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Quantity_Base](Scm_Purchase_Order_Lines.md#quantity_base)|
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

### Confirmed_Quantity_Base


Confirmed_Quantity_Base


The theoretical equivalence of Confirmed Quantity in base measurement unit according to the current measurement dimensions of the product.


The theoretical equivalence of Confirmed Quantity in base measurement unit according to the current measurement dimensions of the product.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Confirmed_Quantity_Base](Scm_Purchase_Order_Lines.md#confirmed_quantity_base)|
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

### Product_Variant_Id


Product_Variant_Id


If specified determines which product variant of the current product in this line is used.


If specified determines which product variant of the current product in this line is used.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Product_Variants](Gen_Product_Variants.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Product_Variant_Id](Scm_Purchase_Order_Lines.md#product_variant_id)|
|Depends On|[Product_Id](#product_id)|
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
|Equals|NULL|yes|yes|

### Lot_Id


Lot_Id


When not null, indicates that a specific lot is required to be delivered.


When not null, indicates that a specific lot is required to be delivered.

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
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Lot_Id](Scm_Purchase_Order_Lines.md#lot_id)|
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
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Row_Version](Scm_Purchase_Order_Lines.md#row_version)|
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

### Parent_Line_No


Parent_Line_No

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
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Parent_Line_No](Scm_Purchase_Order_Lines.md#parent_line_no)|
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

### Parent_Document_Id


Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Parent_Document_Id](Scm_Purchase_Order_Lines.md#parent_document_id)|
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

### Standard_Quantity_Base


Standard_Quantity_Base


The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.


The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Standard_Quantity_Base](Scm_Purchase_Order_Lines.md#standard_quantity_base)|
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

### Confirmed_Standard_Quantity_Base


Confirmed_Standard_Quantity_Base


The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Confirmed Quantity using the measurement ratios.


The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Confirmed Quantity using the measurement ratios.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Order_Lines](Scm_Purchase_Order_Lines.md).[Confirmed_Standard_Quantity_Base](Scm_Purchase_Order_Lines.md#confirmed_standard_quantity_base)|
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


