# Table Sys_Objects

Extends data in other tables with attached files, custom properties, etc. Each row is an object, bound to exactly one row in the primary table. Each object can be bound to a row in a different primary table, specified in Entity_Type. Entity: Sys_Objects

## Summary

| Name | Type | Description |
| - | - | --- |
|[Object_Id](#object_id)|`uniqueidentifier` `PK`|.|
|[Entity_Type](#entity_type)|`nvarchar(64)` |The entity type of the row to which the object is bound|
|[Entity_Item_Id](#entity_item_id)|`uniqueidentifier` |The Id of the primary row to which the object is bound|
|[Latest_Version](#latest_version)|`int` |The latest saved version of the object. Starts from 1 and increments with 1 for each new version.|
|[Row_Version](#row_version)|`timestamp` ||
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact server time (in UTC) when the object represented by this system object was created. NULL means that it is unknown.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` |The user, who created the object represented by this system object . NULL means that it is unknown.|
|[Last_Update_Time_Utc](#last_update_time_utc)|`datetime` |The exact server time (in UTC) of the last modification of the object represented by this system object. NULL means that it is unknown.|
|[Last_Update_User_Id](#last_update_user_id)|`uniqueidentifier` |The user, who made the last modification of the object represented by this system object . NULL means that it is unknown.|
|[Is_Deleted](#is_deleted)|`bit` |Specifies whether the object represented by this system object is deleted. After deletion of the original object, the system object remains in the system, but can be purged later by some cleanup processes.|

## Columns

### Object_Id


Object_Id


.


.

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
|Derived From|[Sys_Objects](Sys_Objects.md).[Object_Id](Sys_Objects.md#object_id)|
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

### Entity_Type


Entity_Type


The entity type of the row to which the object is bound


The entity type of the row to which the object is bound

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value| |
|Derived From|[Sys_Objects](Sys_Objects.md).[Entity_Type](Sys_Objects.md#entity_type)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|yes|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Entity_Item_Id


Entity_Item_Id


The Id of the primary row to which the object is bound


The Id of the primary row to which the object is bound

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Objects](Sys_Objects.md).[Entity_Item_Id](Sys_Objects.md#entity_item_id)|
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

### Latest_Version


Latest_Version


The latest saved version of the object. Starts from 1 and increments with 1 for each new version.


The latest saved version of the object. Starts from 1 and increments with 1 for each new version.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Sys_Objects](Sys_Objects.md).[Latest_Version](Sys_Objects.md#latest_version)|
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
|Derived From|[Sys_Objects](Sys_Objects.md).[Row_Version](Sys_Objects.md#row_version)|
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

### Creation_Time_Utc


Creation_Time_Utc


The exact server time (in UTC) when the object represented by this system object was created. NULL means that it is unknown.


The exact server time (in UTC) when the object represented by this system object was created. NULL means that it is unknown.

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
|Derived From|[Sys_Objects](Sys_Objects.md).[Creation_Time_Utc](Sys_Objects.md#creation_time_utc)|
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
|GreaterThanOrLessThan|None|no|no|

### Creation_User_Id


Creation_User_Id


The user, who created the object represented by this system object . NULL means that it is unknown.


The user, who created the object represented by this system object . NULL means that it is unknown.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Objects](Sys_Objects.md).[Creation_User_Id](Sys_Objects.md#creation_user_id)|
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

### Last_Update_Time_Utc


Last_Update_Time_Utc


The exact server time (in UTC) of the last modification of the object represented by this system object. NULL means that it is unknown.


The exact server time (in UTC) of the last modification of the object represented by this system object. NULL means that it is unknown.

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
|Derived From|[Sys_Objects](Sys_Objects.md).[Last_Update_Time_Utc](Sys_Objects.md#last_update_time_utc)|
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
|GreaterThanOrLessThan|None|no|no|

### Last_Update_User_Id


Last_Update_User_Id


The user, who made the last modification of the object represented by this system object . NULL means that it is unknown.


The user, who made the last modification of the object represented by this system object . NULL means that it is unknown.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Objects](Sys_Objects.md).[Last_Update_User_Id](Sys_Objects.md#last_update_user_id)|
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

### Is_Deleted


Is_Deleted


Specifies whether the object represented by this system object is deleted. After deletion of the original object, the system object remains in the system, but can be purged later by some cleanup processes.


Specifies whether the object represented by this system object is deleted. After deletion of the original object, the system object remains in the system, but can be purged later by some cleanup processes.

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
|Derived From|[Sys_Objects](Sys_Objects.md).[Is_Deleted](Sys_Objects.md#is_deleted)|
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


