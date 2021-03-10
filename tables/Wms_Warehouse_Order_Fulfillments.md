# Table Wms_Warehouse_Order_Fulfillments

Fulfillment of a warehouse order line. Entity: Wms_Warehouse_Order_Fulfillments (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Order_Fulfillment_Id](#warehouse_order_fulfillment_id)|`uniqueidentifier` `PK`||
|[Warehouse_Order_Id](#warehouse_order_id)|`uniqueidentifier` |The warehouse order, which is fulfilled.|
|[Warehouse_Order_Line_Id](#warehouse_order_line_id)|`uniqueidentifier` |The line for which we record fulfillment.|
|[Quantity](#quantity)|`decimal(12, 3)` |Fulfilled quantity in the measurement unit of the warehouse order line.|
|[Is_Final](#is_final)|`bit` |Specifies whether this fulfillment will finalize the fulfillment of the order line, regardless of any remaining quantities.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` |The user, who created the record.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact time in UTC, when the fulfillment was created in the system.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Warehouse_Order_Fulfillment_Id


Warehouse_Order_Fulfillment_Id

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
|Derived From|[Wms_Warehouse_Order_Fulfillments](Wms_Warehouse_Order_Fulfillments.md).[Warehouse_Order_Fulfillment_Id](Wms_Warehouse_Order_Fulfillments.md#warehouse_order_fulfillment_id)|
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

### Warehouse_Order_Id


Warehouse_Order_Id


The warehouse order, which is fulfilled.


The warehouse order, which is fulfilled.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wms_Warehouse_Orders](Wms_Warehouse_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Order_Fulfillments](Wms_Warehouse_Order_Fulfillments.md).[Warehouse_Order_Id](Wms_Warehouse_Order_Fulfillments.md#warehouse_order_id)|
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

### Warehouse_Order_Line_Id


Warehouse_Order_Line_Id


The line for which we record fulfillment.


The line for which we record fulfillment.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wms_Warehouse_Order_Lines](Wms_Warehouse_Order_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Order_Fulfillments](Wms_Warehouse_Order_Fulfillments.md).[Warehouse_Order_Line_Id](Wms_Warehouse_Order_Fulfillments.md#warehouse_order_line_id)|
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


Fulfilled quantity in the measurement unit of the warehouse order line.


Fulfilled quantity in the measurement unit of the warehouse order line.

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
|Derived From|[Wms_Warehouse_Order_Fulfillments](Wms_Warehouse_Order_Fulfillments.md).[Quantity](Wms_Warehouse_Order_Fulfillments.md#quantity)|
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

### Is_Final


Is_Final


Specifies whether this fulfillment will finalize the fulfillment of the order line, regardless of any remaining quantities.


Specifies whether this fulfillment will finalize the fulfillment of the order line, regardless of any remaining quantities.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Order_Fulfillments](Wms_Warehouse_Order_Fulfillments.md).[Is_Final](Wms_Warehouse_Order_Fulfillments.md#is_final)|
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

### Creation_User_Id


Creation_User_Id


The user, who created the record.


The user, who created the record.

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
|Derived From|[Wms_Warehouse_Order_Fulfillments](Wms_Warehouse_Order_Fulfillments.md).[Creation_User_Id](Wms_Warehouse_Order_Fulfillments.md#creation_user_id)|
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

### Creation_Time_Utc


Creation_Time_Utc


The exact time in UTC, when the fulfillment was created in the system.


The exact time in UTC, when the fulfillment was created in the system.

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
|Derived From|[Wms_Warehouse_Order_Fulfillments](Wms_Warehouse_Order_Fulfillments.md).[Creation_Time_Utc](Wms_Warehouse_Order_Fulfillments.md#creation_time_utc)|
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
|Derived From|[Wms_Warehouse_Order_Fulfillments](Wms_Warehouse_Order_Fulfillments.md).[Row_Version](Wms_Warehouse_Order_Fulfillments.md#row_version)|
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


