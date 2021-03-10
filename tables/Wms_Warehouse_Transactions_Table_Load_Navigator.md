# Query Wms_Warehouse_Transactions_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Transaction_Id](#warehouse_transaction_id)|`uniqueidentifier` `PK`||
|[Warehouse_Order_Id](#warehouse_order_id)|`uniqueidentifier` |The order which created this transaction. NULL when this transaction was not based on order.|
|[Warehouse_Order_Line_Id](#warehouse_order_line_id)|`uniqueidentifier` |The order line which created this transaction. NULL when this transaction was not based on order line.|
|[Warehouse_Id](#warehouse_id)|`uniqueidentifier` |The warehouse in which the transaction occurred.|
|[Warehouse_Location_Id](#warehouse_location_id)|`uniqueidentifier` |The warehouse location, where the transaction occurred.|
|[Logistic_Unit_Id](#logistic_unit_id)|`uniqueidentifier` |Logistic unit, which was transacted. NULL when the transaction was not for a logistic unit.|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which was transacted.|
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |The product variant, which was transacted. NULL when the transaction was not for a product variant.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The lot which was transacted. NULL when the transaction was not for a specific lot.|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |The serial number which was transacted. NULL when the transaction was not for a specific serial number.|
|[Direction](#direction)|`nvarchar` Allowed: `I`, `O`|Direction of the transaction - I=IN, O=OUT.|
|[Quantity](#quantity)|`decimal(0, 0)` |The transacted net change in quantity. Positive values indicate transactions. Negative values are used for adjustments.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of quantity.|
|[Catch_Quantity](#catch_quantity)|`decimal(0, 0)` |Catch (measured) quantity for the transaction. Positive values indicate transactions. Negative values are used for adjustments. NULL when catch measurement is not configured for the product.|
|[Catch_Quantity_Unit_Id](#catch_quantity_unit_id)|`uniqueidentifier` |The measurement unit of the catch quantity. NULL when catch measurement is not configured for the product.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` ||
|[Creation_Time_Utc](#creation_time_utc)|`datetime` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Warehouse_Transaction_Id


Warehouse_Transaction_Id

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
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Warehouse_Transaction_Id](Wms_Warehouse_Transactions.md#warehouse_transaction_id)|
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
|Equals|NULL|no|no|

### Warehouse_Order_Id


Warehouse_Order_Id


The order which created this transaction. NULL when this transaction was not based on order.


The order which created this transaction. NULL when this transaction was not based on order.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wms_Warehouse_Orders](Wms_Warehouse_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Warehouse_Order_Id](Wms_Warehouse_Transactions.md#warehouse_order_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Warehouse_Order_Line_Id


Warehouse_Order_Line_Id


The order line which created this transaction. NULL when this transaction was not based on order line.


The order line which created this transaction. NULL when this transaction was not based on order line.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wms_Warehouse_Order_Lines](Wms_Warehouse_Order_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Warehouse_Order_Line_Id](Wms_Warehouse_Transactions.md#warehouse_order_line_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Warehouse_Id


Warehouse_Id


The warehouse in which the transaction occurred.


The warehouse in which the transaction occurred.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wms_Warehouses](Wms_Warehouses.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Warehouse_Id](Wms_Warehouse_Transactions.md#warehouse_id)|
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

### Warehouse_Location_Id


Warehouse_Location_Id


The warehouse location, where the transaction occurred.


The warehouse location, where the transaction occurred.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wms_Warehouse_Locations](Wms_Warehouse_Locations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Warehouse_Location_Id](Wms_Warehouse_Transactions.md#warehouse_location_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Logistic_Unit_Id


Logistic_Unit_Id


Logistic unit, which was transacted. NULL when the transaction was not for a logistic unit.


Logistic unit, which was transacted. NULL when the transaction was not for a logistic unit.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Log_Logistic_Units](Log_Logistic_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Logistic_Unit_Id](Wms_Warehouse_Transactions.md#logistic_unit_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Product_Id


Product_Id


The product, which was transacted.


The product, which was transacted.

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
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Product_Id](Wms_Warehouse_Transactions.md#product_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Product_Variant_Id


Product_Variant_Id


The product variant, which was transacted. NULL when the transaction was not for a product variant.


The product variant, which was transacted. NULL when the transaction was not for a product variant.

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
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Product_Variant_Id](Wms_Warehouse_Transactions.md#product_variant_id)|
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


The lot which was transacted. NULL when the transaction was not for a specific lot.


The lot which was transacted. NULL when the transaction was not for a specific lot.

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
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Lot_Id](Wms_Warehouse_Transactions.md#lot_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Serial_Number_Id


Serial_Number_Id


The serial number which was transacted. NULL when the transaction was not for a specific serial number.


The serial number which was transacted. NULL when the transaction was not for a specific serial number.

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
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Serial_Number_Id](Wms_Warehouse_Transactions.md#serial_number_id)|
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
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Direction


Direction


Direction of the transaction - I=IN, O=OUT.


Direction of the transaction - I=IN, O=OUT.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`I`, `O`|
|Default Value|I|
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Direction](Wms_Warehouse_Transactions.md#direction)|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Quantity


Quantity


The transacted net change in quantity. Positive values indicate transactions. Negative values are used for adjustments.


The transacted net change in quantity. Positive values indicate transactions. Negative values are used for adjustments.

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Quantity](Wms_Warehouse_Transactions.md#quantity)|
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
|Order|11|
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


The measurement unit of quantity.


The measurement unit of quantity.

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
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Quantity_Unit_Id](Wms_Warehouse_Transactions.md#quantity_unit_id)|
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
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Catch_Quantity


Catch_Quantity


Catch (measured) quantity for the transaction. Positive values indicate transactions. Negative values are used for adjustments. NULL when catch measurement is not configured for the product.


Catch (measured) quantity for the transaction. Positive values indicate transactions. Negative values are used for adjustments. NULL when catch measurement is not configured for the product.

| Property | Value |
| - | - |
|Type|decimal(0, 0)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Catch_Quantity](Wms_Warehouse_Transactions.md#catch_quantity)|
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
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|GreaterThanOrLessThan|None|yes|no|

### Catch_Quantity_Unit_Id


Catch_Quantity_Unit_Id


The measurement unit of the catch quantity. NULL when catch measurement is not configured for the product.


The measurement unit of the catch quantity. NULL when catch measurement is not configured for the product.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Catch_Quantity_Unit_Id](Wms_Warehouse_Transactions.md#catch_quantity_unit_id)|
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
|Order|14|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Creation_User_Id


Creation_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Creation_User_Id](Wms_Warehouse_Transactions.md#creation_user_id)|
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
|Order|15|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Creation_Time_Utc


Creation_Time_Utc

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
|Default Value|CurrentDateTimeUtc|
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Creation_Time_Utc](Wms_Warehouse_Transactions.md#creation_time_utc)|
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
|Order|16|
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
|Derived From|[Wms_Warehouse_Transactions](Wms_Warehouse_Transactions.md).[Row_Version](Wms_Warehouse_Transactions.md#row_version)|
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
|Order|17|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


