# Table Wms_Warehouse_Requisition_Fulfillments


## Entity

Entity: [Logistics.Wms.WarehouseRequisitionFulfillments](~/entities/Logistics.Wms.WarehouseRequisitionFulfillments.md)

Fulfillment ledger for warehouse requisitions. Entity: Wms_Warehouse_Requisition_Fulfillments (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[__Object_Version](#__object_version)|`int` ||
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact time in UTC, when the fulfillment was created in the system.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` |The user, who created the record.|
|[Fulfillment_Type](#fulfillment_type)|`nvarchar(1)` |Type of fulfillment: P=Plan created; C=Requisition completed.|
|[Is_Final](#is_final)|`bit` |Specifies whether this fulfillment finalizes the requisition line, regardless of any remaining quantities.|
|[Quantity](#quantity)|`decimal(12, 3)` |Quantity fulfilled (in the measurement unit of the requisition line).|
|[Row_Version](#row_version)|`timestamp` ||
|[Warehouse_Requisition_Fulfillment_Id](#warehouse_requisition_fulfillment_id)|`uniqueidentifier` `PK`||
|[Warehouse_Requisition_Id](#warehouse_requisition_id)|`uniqueidentifier` |The warehouse requisiton, which is fulfilled.|
|[Warehouse_Requisition_Line_Id](#warehouse_requisition_line_id)|`uniqueidentifier` |The requisition line, which is fulfilled.|

## Columns

### __Object_Version

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|None|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|-1|
|Order|2147483647|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|no|
|Type|int (Allows NULL)|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|no|

### Creation_Time_Utc


The exact time in UTC, when the fulfillment was created in the system.

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|None|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|-1|
|Order|2147483647|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|no|
|Type|datetime|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|yes|

### Creation_User_Id


The user, who created the record.

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|None|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|-1|
|Order|2147483647|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|yes|
|Type|uniqueidentifier|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|yes|

#### Creation_User_Id - Supported Filters

| Filter Type | Default | Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|`NULL`|no|no|

### Fulfillment_Type


Type of fulfillment: P=Plan created; C=Requisition completed.

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|None|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|1|
|Order|2147483647|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|no|
|Type|nvarchar(1)|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|yes|

### Is_Final


Specifies whether this fulfillment finalizes the requisition line, regardless of any remaining quantities.

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|None|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|-1|
|Order|2147483647|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|no|
|Type|bit|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|yes|

### Quantity


Quantity fulfilled (in the measurement unit of the requisition line).

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|None|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|-1|
|Order|2147483647|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|no|
|Type|decimal(12, 3)|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|yes|

### Row_Version

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|None|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|-1|
|Order|2147483647|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|no|
|Type|timestamp|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|no|

### Warehouse_Requisition_Fulfillment_Id

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|NewGuid|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|-1|
|Order|2147483647|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|yes (order: 1)|
|Readonly|no|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|yes|
|Type|uniqueidentifier|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|yes|

#### Warehouse_Requisition_Fulfillment_Id - Supported Filters

| Filter Type | Default | Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|`NULL`|no|no|

### Warehouse_Requisition_Id


The warehouse requisiton, which is fulfilled.

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|None|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|-1|
|Order|2147483647|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|Referenced Table|[Wms_Warehouse_Requisitions](Wms_Warehouse_Requisitions.md)|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|yes|
|Type|uniqueidentifier|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|yes|

#### Warehouse_Requisition_Id - Supported Filters

| Filter Type | Default | Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|`NULL`|no|no|

### Warehouse_Requisition_Line_Id


The requisition line, which is fulfilled.

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|None|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|-1|
|Order|2147483647|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|Referenced Table|[Wms_Warehouse_Requisition_Lines](Wms_Warehouse_Requisition_Lines.md)|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|yes|
|Type|uniqueidentifier|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|yes|

#### Warehouse_Requisition_Line_Id - Supported Filters

| Filter Type | Default | Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|`NULL`|no|no|


