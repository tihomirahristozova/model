# Table Prd_Consumption_Order_Lines

Detail lines of orders for material consumption. Entity: Prd_Consumption_Order_Lines

## Owner Tables Hierarchy

* [Prd_Consumption_Orders](Prd_Consumption_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Ord](#line_ord)|`int` |Non-unique line number within the order|
|[Work_Order_Item_Ingredient_Id](#work_order_item_ingredient_id)|`uniqueidentifier` |The Work Order Item Ingredient for which we are ordering materials.|
|[Scheduled_Date_Time](#scheduled_date_time)|`datetime` |The scheduled date, when the material is needed.|
|[Product_Id](#product_id)|`uniqueidentifier` |The requested material.|
|[Consumed_Quantity](#consumed_quantity)|`decimal(18, 3)` |Requested quantity of the material.|
|[Consumed_Quantity_Unit_Id](#consumed_quantity_unit_id)|`uniqueidentifier` |Measurement unit of the requested quantity.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store, from which the material is requested.|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |If not NULL, specifies that the material has to be consumed from specific store bin|
|[Lot_Id](#lot_id)|`uniqueidentifier` |If not NULL, specifies that the material has to be consumed from specific lot|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |If not NULL, specifies that the material has to be consumed with specific serial number|
|[Consumption_Type](#consumption_type)|`nvarchar(1)` Allowed: `S`, `A`, Readonly|Determines whether the material cost is distributed among all produced products, or only one (specified in the Work Order Item Ingredient).|
|[Consumed_Quantity_Base](#consumed_quantity_base)|`decimal(18, 3)` Readonly|The requested quantity equivalence in the base measurement category of the requested material.|
|[Consumption_Order_Id](#consumption_order_id)|`uniqueidentifier` ||
|[Id](#id)|`uniqueidentifier` `PK`|Unique order lline Id|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Consumed_Standard_Quantity_Base](#consumed_standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Quantity using the measurement ratios.|

## Columns

### Line_Ord


Line_Ord


Non-unique line number within the order


Non-unique line number within the order

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
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Line_Ord](Prd_Consumption_Order_Lines.md#line_ord)|
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

### Work_Order_Item_Ingredient_Id


Work_Order_Item_Ingredient_Id


The Work Order Item Ingredient for which we are ordering materials.


The Work Order Item Ingredient for which we are ordering materials.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Work_Order_Item_Ingredients](Prd_Work_Order_Item_Ingredients.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Work_Order_Item_Ingredient_Id](Prd_Consumption_Order_Lines.md#work_order_item_ingredient_id)|
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

### Scheduled_Date_Time


Scheduled_Date_Time


The scheduled date, when the material is needed.


The scheduled date, when the material is needed.

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
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Scheduled_Date_Time](Prd_Consumption_Order_Lines.md#scheduled_date_time)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Product_Id


Product_Id


The requested material.


The requested material.

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
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Product_Id](Prd_Consumption_Order_Lines.md#product_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Consumed_Quantity


Consumed_Quantity


Requested quantity of the material.


Requested quantity of the material.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Consumed_Quantity](Prd_Consumption_Order_Lines.md#consumed_quantity)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Consumed_Quantity_Unit_Id


Consumed_Quantity_Unit_Id


Measurement unit of the requested quantity.


Measurement unit of the requested quantity.

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
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Consumed_Quantity_Unit_Id](Prd_Consumption_Order_Lines.md#consumed_quantity_unit_id)|
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
|UI Width|Short|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Store_Id


Store_Id


The store, from which the material is requested.


The store, from which the material is requested.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Stores](Inv_Stores.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Store_Id](Prd_Consumption_Order_Lines.md#store_id)|
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

### Store_Bin_Id


Store_Bin_Id


If not NULL, specifies that the material has to be consumed from specific store bin


If not NULL, specifies that the material has to be consumed from specific store bin

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
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Store_Bin_Id](Prd_Consumption_Order_Lines.md#store_bin_id)|
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

### Lot_Id


Lot_Id


If not NULL, specifies that the material has to be consumed from specific lot


If not NULL, specifies that the material has to be consumed from specific lot

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
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Lot_Id](Prd_Consumption_Order_Lines.md#lot_id)|
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
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Serial_Number_Id


Serial_Number_Id


If not NULL, specifies that the material has to be consumed with specific serial number


If not NULL, specifies that the material has to be consumed with specific serial number

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
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Serial_Number_Id](Prd_Consumption_Order_Lines.md#serial_number_id)|
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
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Consumption_Type


Consumption_Type


Determines whether the material cost is distributed among all produced products, or only one (specified in the Work Order Item Ingredient).


Determines whether the material cost is distributed among all produced products, or only one (specified in the Work Order Item Ingredient).

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Allowed Values|`S`, `A`|
|Default Value|None|
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Consumption_Type](Prd_Consumption_Order_Lines.md#consumption_type)|
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
|Max Length|1|
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Consumed_Quantity_Base


Consumed_Quantity_Base


The requested quantity equivalence in the base measurement category of the requested material.


The requested quantity equivalence in the base measurement category of the requested material.

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
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Consumed_Quantity_Base](Prd_Consumption_Order_Lines.md#consumed_quantity_base)|
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
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Consumption_Order_Id


Consumption_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Prd_Consumption_Orders](Prd_Consumption_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Consumption_Order_Id](Prd_Consumption_Order_Lines.md#consumption_order_id)|
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
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Id


Id


Unique order lline Id


Unique order lline Id

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
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Id](Prd_Consumption_Order_Lines.md#id)|
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
|Order|13|
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
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Notes](Prd_Consumption_Order_Lines.md#notes)|
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
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Row_Version](Prd_Consumption_Order_Lines.md#row_version)|
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

### Consumed_Standard_Quantity_Base


Consumed_Standard_Quantity_Base


The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Quantity using the measurement ratios.


The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Quantity using the measurement ratios.

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
|Derived From|[Prd_Consumption_Order_Lines](Prd_Consumption_Order_Lines.md).[Consumed_Standard_Quantity_Base](Prd_Consumption_Order_Lines.md#consumed_standard_quantity_base)|
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


