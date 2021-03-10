# Table Log_Shipment_Lines

Represents detail lines of shipments. Each line contains the shipment of one product. Entity: Log_Shipment_Lines

## Owner Tables Hierarchy

* [Log_Shipments](Log_Shipments.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Shipment_Line_Id](#shipment_line_id)|`uniqueidentifier` `PK`||
|[Shipment_Id](#shipment_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Line number, unique for the shipment|
|[Shipment_Order_Line_Id](#shipment_order_line_id)|`uniqueidentifier` |Shipment order line for which this quantity is shipped|
|[Parent_Sales_Order_Line_Id](#parent_sales_order_line_id)|`uniqueidentifier` |Sales order line which is shipped|
|[Quantity](#quantity)|`decimal(12, 3)` |The quantity to be shipped|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Finished](#finished)|`bit` |1 if this shipment should prohibit further shipments for the sales order line|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |The store bin from which to take the goods|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The store lot from which to take the goods|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |The serial number of the shipped product. NULL means that serial number is unknown or not applicable.|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Guarantee period in days for the offered product. NULL for non-serviced products|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Quantity_Base](#quantity_base)|`decimal(12, 3)` |The equivalence of Quantity in the base measurement category of the product.|
|[Transaction_Line_Id](#transaction_line_id)|`uniqueidentifier` |The Transaction Line, based on which this shipment line was created. The transaction line contains the store issue operation of the shipped product.|
|[Line_Required_Delivery_Date](#line_required_delivery_date)|`datetime` |Required delivery date for this lines. Depending on the shipment route travel time, the shipment should be released accordingly|
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute parent line.|
|[Length_m](#length_m)|`decimal(12, 3)` |The length of the package in meters. NULL means unknown|
|[Pallet_No](#pallet_no)|`int` |The number of the pallet in which the goods are packaged. NULL means unknown|
|[Width_m](#width_m)|`decimal(12, 3)` |The width of the package in meters. NULL means unknown|
|[Row_Version](#row_version)|`timestamp` ||
|[Height_m](#height_m)|`decimal(12, 3)` |The height of the package in meters. NULL means unknown|
|[Volume_l](#volume_l)|`decimal(12, 3)` |The volume in litres of the whole batch. NULL means unknown|
|[Gross_Weight_kg](#gross_weight_kg)|`decimal(12, 3)` |The gross weight of the whole line in kilogramms. NULL means unknown|
|[Net_Weight_kg](#net_weight_kg)|`decimal(12, 3)` |The net weight of the entire batch of goods in kilograms. NULL means unknown|
|[Box_Count](#box_count)|`int` |The count of boxes in which the goods are packaged. NULL means unknown|
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(12, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

## Columns

### Shipment_Line_Id


Shipment_Line_Id

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Shipment_Line_Id](Log_Shipment_Lines.md#shipment_line_id)|
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

### Shipment_Id


Shipment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Log_Shipments](Log_Shipments.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Shipment_Id](Log_Shipment_Lines.md#shipment_id)|
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
|Order|1|
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


Line number, unique for the shipment


Line number, unique for the shipment

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Line_No](Log_Shipment_Lines.md#line_no)|
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
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Shipment_Order_Line_Id


Shipment_Order_Line_Id


Shipment order line for which this quantity is shipped


Shipment order line for which this quantity is shipped

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Log_Shipment_Order_Lines](Log_Shipment_Order_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Shipment_Order_Line_Id](Log_Shipment_Lines.md#shipment_order_line_id)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Parent_Sales_Order_Line_Id


Parent_Sales_Order_Line_Id


Sales order line which is shipped


Sales order line which is shipped

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Sales_Order_Lines](Crm_Sales_Order_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Parent_Sales_Order_Line_Id](Log_Shipment_Lines.md#parent_sales_order_line_id)|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Quantity


Quantity


The quantity to be shipped


The quantity to be shipped

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Quantity](Log_Shipment_Lines.md#quantity)|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|101|
|Supports EQUALS_IN|no|

### Quantity_Unit_Id


Quantity_Unit_Id


The measurement unit of Quantity


The measurement unit of Quantity

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Quantity_Unit_Id](Log_Shipment_Lines.md#quantity_unit_id)|
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
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Finished


Finished


1 if this shipment should prohibit further shipments for the sales order line


1 if this shipment should prohibit further shipments for the sales order line

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Finished](Log_Shipment_Lines.md#finished)|
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
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Store_Bin_Id


Store_Bin_Id


The store bin from which to take the goods


The store bin from which to take the goods

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Store_Bins](Inv_Store_Bins.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Store_Bin_Id](Log_Shipment_Lines.md#store_bin_id)|
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
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Lot_Id


Lot_Id


The store lot from which to take the goods


The store lot from which to take the goods

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Lot_Id](Log_Shipment_Lines.md#lot_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Serial_Number_Id


Serial_Number_Id


The serial number of the shipped product. NULL means that serial number is unknown or not applicable.


The serial number of the shipped product. NULL means that serial number is unknown or not applicable.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Serial_Numbers](Inv_Serial_Numbers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Serial_Number_Id](Log_Shipment_Lines.md#serial_number_id)|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Guarantee_Period_Days](Log_Shipment_Lines.md#guarantee_period_days)|
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
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Parent_Document_Id


Parent_Document_Id


The document, which the current line executes. NULL when the current line does not execute another line.


The document, which the current line executes. NULL when the current line does not execute another line.

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Parent_Document_Id](Log_Shipment_Lines.md#parent_document_id)|
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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Notes](Log_Shipment_Lines.md#notes)|
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

### Quantity_Base


Quantity_Base


The equivalence of Quantity in the base measurement category of the product.


The equivalence of Quantity in the base measurement category of the product.

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Quantity_Base](Log_Shipment_Lines.md#quantity_base)|
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

### Transaction_Line_Id


Transaction_Line_Id


The Transaction Line, based on which this shipment line was created. The transaction line contains the store issue operation of the shipped product.


The Transaction Line, based on which this shipment line was created. The transaction line contains the store issue operation of the shipped product.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Transaction_Lines](Inv_Transaction_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Transaction_Line_Id](Log_Shipment_Lines.md#transaction_line_id)|
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

### Line_Required_Delivery_Date


Line_Required_Delivery_Date


Required delivery date for this lines. Depending on the shipment route travel time, the shipment should be released accordingly


Required delivery date for this lines. Depending on the shipment route travel time, the shipment should be released accordingly

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Line_Required_Delivery_Date](Log_Shipment_Lines.md#line_required_delivery_date)|
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

### Parent_Line_No


Parent_Line_No


The number of the line within the parent document, which the current line executes. NULL when the current line does not execute parent line.


The number of the line within the parent document, which the current line executes. NULL when the current line does not execute parent line.

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Parent_Line_No](Log_Shipment_Lines.md#parent_line_no)|
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

### Length_m


Length_m


The length of the package in meters. NULL means unknown


The length of the package in meters. NULL means unknown

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Length_m](Log_Shipment_Lines.md#length_m)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Pallet_No


Pallet_No


The number of the pallet in which the goods are packaged. NULL means unknown


The number of the pallet in which the goods are packaged. NULL means unknown

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Pallet_No](Log_Shipment_Lines.md#pallet_no)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Width_m


Width_m


The width of the package in meters. NULL means unknown


The width of the package in meters. NULL means unknown

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Width_m](Log_Shipment_Lines.md#width_m)|
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
|UI Width|100|
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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Row_Version](Log_Shipment_Lines.md#row_version)|
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

### Height_m


Height_m


The height of the package in meters. NULL means unknown


The height of the package in meters. NULL means unknown

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Height_m](Log_Shipment_Lines.md#height_m)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Volume_l


Volume_l


The volume in litres of the whole batch. NULL means unknown


The volume in litres of the whole batch. NULL means unknown

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Volume_l](Log_Shipment_Lines.md#volume_l)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Gross_Weight_kg


Gross_Weight_kg


The gross weight of the whole line in kilogramms. NULL means unknown


The gross weight of the whole line in kilogramms. NULL means unknown

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Gross_Weight_kg](Log_Shipment_Lines.md#gross_weight_kg)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Net_Weight_kg


Net_Weight_kg


The net weight of the entire batch of goods in kilograms. NULL means unknown


The net weight of the entire batch of goods in kilograms. NULL means unknown

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Net_Weight_kg](Log_Shipment_Lines.md#net_weight_kg)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Box_Count


Box_Count


The count of boxes in which the goods are packaged. NULL means unknown


The count of boxes in which the goods are packaged. NULL means unknown

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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Box_Count](Log_Shipment_Lines.md#box_count)|
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
|UI Width|100|
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
|Derived From|[Log_Shipment_Lines](Log_Shipment_Lines.md).[Standard_Quantity_Base](Log_Shipment_Lines.md#standard_quantity_base)|
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


