# Query Sys_Attribute_Changes_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Time_Utc](#time_utc)|`datetime` |Date and time (in Utc) when the changeset was processed by the server.|
|[User_Id](#user_id)|`uniqueidentifier` |The user which initiated the change. NULL when it is unknown.|
|[Application_Name](#application_name)|`nvarchar` |The application which requested the change. NULL when it is unknown.|
|[Server_Version](#server_version)|`nvarchar` |The version of the application server at the time of the change.|
|[Object_Changeset_Id](#object_changeset_id)|`uniqueidentifier` |The changeset containing this change.|
|[Root_Object_Id](#root_object_id)|`uniqueidentifier` |The root object in the aggregate of the object, which has been changed. Each change is recorded at the aggregate root level.|
|[Repository_Name](#repository_name)|`nvarchar` |The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object.|
|[Entity_Item_Id](#entity_item_id)|`uniqueidentifier` |The id of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object.|
|[Change_Type](#change_type)|`nvarchar` Allowed: `C`, `U`, `D`|Type of change - Create, Update or Delete.|
|[Old_Values_Json](#old_values_json)|`nvarchar` |Old values in a name-value Json format. Only changed data attributes are recorded. Old values are recorded for update and delete.|
|[Object_Change_Id](#object_change_id)|`uniqueidentifier` `PK`||
|[Attribute_Name](#attribute_name)|`nvarchar` `PK`||
|[New_Value](#new_value)|`nvarchar` ||
|[Entity_Type](#entity_type)|`nvarchar` |The entity type of the row to which the object is bound|
|[Object_Entity_Item_Id](#object_entity_item_id)|`uniqueidentifier` |The Id of the primary row to which the object is bound|
|[Latest_Version](#latest_version)|`int` |The latest saved version of the object. Starts from 1 and increments with 1 for each new version.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact server time (in UTC) when the object represented by this system object was created. NULL means that it is unknown.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` |The user, who created the object represented by this system object . NULL means that it is unknown.|
|[Last_Update_Time_Utc](#last_update_time_utc)|`datetime` |The exact server time (in UTC) of the last modification of the object represented by this system object. NULL means that it is unknown.|
|[Last_Update_User_Id](#last_update_user_id)|`uniqueidentifier` |The user, who made the last modification of the object represented by this system object . NULL means that it is unknown.|
|[Is_Deleted](#is_deleted)|`bit` |Specifies whether the object represented by this system object is deleted. After deletion of the original object, the system object remains in the system, but can be purged later by some cleanup processes.|

## Columns

### Time_Utc


Time_Utc


Date and time (in Utc) when the changeset was processed by the server.


Date and time (in Utc) when the changeset was processed by the server.

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
|Derived From|[Sys_Object_Changesets](Sys_Object_Changesets.md).[Time_Utc](Sys_Object_Changesets.md#time_utc)|
|Format|g|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|GreaterThanOrLessThan|None|no|no|

### User_Id


User_Id


The user which initiated the change. NULL when it is unknown.


The user which initiated the change. NULL when it is unknown.

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
|Derived From|[Sys_Object_Changesets](Sys_Object_Changesets.md).[User_Id](Sys_Object_Changesets.md#user_id)|
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

### Application_Name


Application_Name


The application which requested the change. NULL when it is unknown.


The application which requested the change. NULL when it is unknown.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Changesets](Sys_Object_Changesets.md).[Application_Name](Sys_Object_Changesets.md#application_name)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Server_Version


Server_Version


The version of the application server at the time of the change.


The version of the application server at the time of the change.

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
|Default Value|None|
|Derived From|[Sys_Object_Changesets](Sys_Object_Changesets.md).[Server_Version](Sys_Object_Changesets.md#server_version)|
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
|Supports EQUALS_IN|no|

### Object_Changeset_Id


Object_Changeset_Id


The changeset containing this change.


The changeset containing this change.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sys_Object_Changesets](Sys_Object_Changesets.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Changes](Sys_Object_Changes.md).[Object_Changeset_Id](Sys_Object_Changes.md#object_changeset_id)|
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

### Root_Object_Id


Root_Object_Id


The root object in the aggregate of the object, which has been changed. Each change is recorded at the aggregate root level.


The root object in the aggregate of the object, which has been changed. Each change is recorded at the aggregate root level.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sys_Objects](Sys_Objects.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Changes](Sys_Object_Changes.md).[Root_Object_Id](Sys_Object_Changes.md#root_object_id)|
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
|Equals|NULL|no|no|

### Repository_Name


Repository_Name


The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object.


The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object.

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
|Default Value|None|
|Derived From|[Sys_Object_Changes](Sys_Object_Changes.md).[Repository_Name](Sys_Object_Changes.md#repository_name)|
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
|Like|None|no|no|

### Entity_Item_Id


Entity_Item_Id


The id of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object.


The id of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object.

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
|Derived From|[Sys_Object_Changes](Sys_Object_Changes.md).[Entity_Item_Id](Sys_Object_Changes.md#entity_item_id)|
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
|Equals|NULL|no|no|

### Change_Type


Change_Type


Type of change - Create, Update or Delete.


Type of change - Create, Update or Delete.

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
|Allowed Values|`C`, `U`, `D`|
|Default Value|None|
|Derived From|[Sys_Object_Changes](Sys_Object_Changes.md).[Change_Type](Sys_Object_Changes.md#change_type)|
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
|Supports EQUALS_IN|no|

### Old_Values_Json


Old_Values_Json


Old values in a name-value Json format. Only changed data attributes are recorded. Old values are recorded for update and delete.


Old values in a name-value Json format. Only changed data attributes are recorded. Old values are recorded for update and delete.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Changes](Sys_Object_Changes.md).[Old_Values_Json](Sys_Object_Changes.md#old_values_json)|
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
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Object_Change_Id


Object_Change_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Referenced Table|[Sys_Object_Changes](Sys_Object_Changes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Attribute_Changes](Sys_Attribute_Changes.md).[Object_Change_Id](Sys_Attribute_Changes.md#object_change_id)|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Attribute_Name


Attribute_Name

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|2|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Attribute_Changes](Sys_Attribute_Changes.md).[Attribute_Name](Sys_Attribute_Changes.md#attribute_name)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### New_Value


New_Value

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Attribute_Changes](Sys_Attribute_Changes.md).[New_Value](Sys_Attribute_Changes.md#new_value)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|Like|None|no|no|

### Entity_Type


Entity_Type


The entity type of the row to which the object is bound


The entity type of the row to which the object is bound

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
|Max Length|-1|
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Object_Entity_Item_Id


Object_Entity_Item_Id


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
|Order|14|
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
|Order|15|
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
|Order|16|
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
|Order|17|
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
|Order|18|
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
|Order|19|
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
|Order|20|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|


