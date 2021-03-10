# Table Wms_Warehouse_Requisition_Fulfillments

Fulfillment ledger for warehouse requisitions. Entity: Wms_Warehouse_Requisition_Fulfillments (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Requisition_Fulfillment_Id](#warehouse_requisition_fulfillment_id)|`uniqueidentifier` `PK`||
|[Warehouse_Requisition_Id](#warehouse_requisition_id)|`uniqueidentifier` |The warehouse requisiton, which is fulfilled.|
|[Warehouse_Requisition_Line_Id](#warehouse_requisition_line_id)|`uniqueidentifier` |The requisition line, which is fulfilled.|
|[Fulfillment_Type](#fulfillment_type)|`nvarchar(1)` |Type of fulfillment: P=Plan created; C=Requisition completed.|
|[Quantity](#quantity)|`decimal(12, 3)` |Quantity fulfilled (in the measurement unit of the requisition line).|
|[Is_Final](#is_final)|`bit` |Specifies whether this fulfillment finalizes the requisition line, regardless of any remaining quantities.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` |The user, who created the record.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact time in UTC, when the fulfillment was created in the system.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Warehouse_Requisition_Fulfillment_Id


Warehouse_Requisition_Fulfillment_Id

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
|Derived From|[Wms_Warehouse_Requisition_Fulfillments](Wms_Warehouse_Requisition_Fulfillments.md).[Warehouse_Requisition_Fulfillment_Id](Wms_Warehouse_Requisition_Fulfillments.md#warehouse_requisition_fulfillment_id)|
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

### Warehouse_Requisition_Id


Warehouse_Requisition_Id


The warehouse requisiton, which is fulfilled.


The warehouse requisiton, which is fulfilled.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wms_Warehouse_Requisitions](Wms_Warehouse_Requisitions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Requisition_Fulfillments](Wms_Warehouse_Requisition_Fulfillments.md).[Warehouse_Requisition_Id](Wms_Warehouse_Requisition_Fulfillments.md#warehouse_requisition_id)|
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

### Warehouse_Requisition_Line_Id


Warehouse_Requisition_Line_Id


The requisition line, which is fulfilled.


The requisition line, which is fulfilled.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wms_Warehouse_Requisition_Lines](Wms_Warehouse_Requisition_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Wms_Warehouse_Requisition_Fulfillments](Wms_Warehouse_Requisition_Fulfillments.md).[Warehouse_Requisition_Line_Id](Wms_Warehouse_Requisition_Fulfillments.md#warehouse_requisition_line_id)|
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

### Fulfillment_Type


Fulfillment_Type


Type of fulfillment: P=Plan created; C=Requisition completed.


Type of fulfillment: P=Plan created; C=Requisition completed.

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
|Default Value|None|
|Derived From|[Wms_Warehouse_Requisition_Fulfillments](Wms_Warehouse_Requisition_Fulfillments.md).[Fulfillment_Type](Wms_Warehouse_Requisition_Fulfillments.md#fulfillment_type)|
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

### Quantity


Quantity


Quantity fulfilled (in the measurement unit of the requisition line).


Quantity fulfilled (in the measurement unit of the requisition line).

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
|Derived From|[Wms_Warehouse_Requisition_Fulfillments](Wms_Warehouse_Requisition_Fulfillments.md).[Quantity](Wms_Warehouse_Requisition_Fulfillments.md#quantity)|
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


Specifies whether this fulfillment finalizes the requisition line, regardless of any remaining quantities.


Specifies whether this fulfillment finalizes the requisition line, regardless of any remaining quantities.

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
|Derived From|[Wms_Warehouse_Requisition_Fulfillments](Wms_Warehouse_Requisition_Fulfillments.md).[Is_Final](Wms_Warehouse_Requisition_Fulfillments.md#is_final)|
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
|Derived From|[Wms_Warehouse_Requisition_Fulfillments](Wms_Warehouse_Requisition_Fulfillments.md).[Creation_User_Id](Wms_Warehouse_Requisition_Fulfillments.md#creation_user_id)|
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
|Derived From|[Wms_Warehouse_Requisition_Fulfillments](Wms_Warehouse_Requisition_Fulfillments.md).[Creation_Time_Utc](Wms_Warehouse_Requisition_Fulfillments.md#creation_time_utc)|
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
|Derived From|[Wms_Warehouse_Requisition_Fulfillments](Wms_Warehouse_Requisition_Fulfillments.md).[Row_Version](Wms_Warehouse_Requisition_Fulfillments.md#row_version)|
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


