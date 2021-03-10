# Table Sys_Resolved_Conflicts

Contains records of conflicts, which were automatically resolved by update procedures. Entity: Sys_Resolved_Conflicts

## Summary

| Name | Type | Description |
| - | - | --- |
|[Resolved_Conflict_Id](#resolved_conflict_id)|`uniqueidentifier` `PK`|Unique identification of the resolved conflict.|
|[URL](#url)|`nvarchar(254)` Readonly|URL of the item (the row) for which the conflict occurred.|
|[Table_Name](#table_name)|`nvarchar(64)` `ML`, Readonly|Name of the table in which the conflict has occurred.|
|[Conflict_Description](#conflict_description)|`nvarchar(400)` `ML`, Readonly|Description of the conflict.|
|[Resolve_Description](#resolve_description)|`nvarchar(400)` `ML`, Readonly|Description of the resolution of the conflict.|
|[Resolved_Time](#resolved_time)|`datetime` Readonly|Time when the resolution of the conflict was made.|
|[Revised_By_User](#revised_by_user)|`bit` Readonly|True, when the conflict resolution was revised (reviewed) manually by user.|
|[Resolve_Confirmed_By_User](#resolve_confirmed_by_user)|`bit` |True, when the conflict resolution was manually confirmed by user.|
|[Resolve_Confirmed_Time](#resolve_confirmed_time)|`datetime` Readonly|Time when the conflict resolution was confirmed by the user.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Resolved_Conflict_Id


Resolved_Conflict_Id


Unique identification of the resolved conflict.


Unique identification of the resolved conflict.

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
|Derived From|[Sys_Resolved_Conflicts](Sys_Resolved_Conflicts.md).[Resolved_Conflict_Id](Sys_Resolved_Conflicts.md#resolved_conflict_id)|
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

### URL


URL


URL of the item (the row) for which the conflict occurred.


URL of the item (the row) for which the conflict occurred.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Resolved_Conflicts](Sys_Resolved_Conflicts.md).[URL](Sys_Resolved_Conflicts.md#url)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Table_Name


Table_Name


Name of the table in which the conflict has occurred.


Name of the table in which the conflict has occurred.

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Resolved_Conflicts](Sys_Resolved_Conflicts.md).[Table_Name](Sys_Resolved_Conflicts.md#table_name)|
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
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Conflict_Description


Conflict_Description


Description of the conflict.


Description of the conflict.

| Property | Value |
| - | - |
|Type|nvarchar(400)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Sys_Resolved_Conflicts](Sys_Resolved_Conflicts.md).[Conflict_Description](Sys_Resolved_Conflicts.md#conflict_description)|
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
|Max Length|400|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Resolve_Description


Resolve_Description


Description of the resolution of the conflict.


Description of the resolution of the conflict.

| Property | Value |
| - | - |
|Type|nvarchar(400)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Sys_Resolved_Conflicts](Sys_Resolved_Conflicts.md).[Resolve_Description](Sys_Resolved_Conflicts.md#resolve_description)|
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
|Max Length|400|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Resolved_Time


Resolved_Time


Time when the resolution of the conflict was made.


Time when the resolution of the conflict was made.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTime|
|Derived From|[Sys_Resolved_Conflicts](Sys_Resolved_Conflicts.md).[Resolved_Time](Sys_Resolved_Conflicts.md#resolved_time)|
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
|Supports EQUALS_IN|no|

### Revised_By_User


Revised_By_User


True, when the conflict resolution was revised (reviewed) manually by user.


True, when the conflict resolution was revised (reviewed) manually by user.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sys_Resolved_Conflicts](Sys_Resolved_Conflicts.md).[Revised_By_User](Sys_Resolved_Conflicts.md#revised_by_user)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|yes|
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
|Equals|NULL|no|no|

### Resolve_Confirmed_By_User


Resolve_Confirmed_By_User


True, when the conflict resolution was manually confirmed by user.


True, when the conflict resolution was manually confirmed by user.

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
|Derived From|[Sys_Resolved_Conflicts](Sys_Resolved_Conflicts.md).[Resolve_Confirmed_By_User](Sys_Resolved_Conflicts.md#resolve_confirmed_by_user)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|yes|
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
|Equals|NULL|no|no|

### Resolve_Confirmed_Time


Resolve_Confirmed_Time


Time when the conflict resolution was confirmed by the user.


Time when the conflict resolution was confirmed by the user.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Resolved_Conflicts](Sys_Resolved_Conflicts.md).[Resolve_Confirmed_Time](Sys_Resolved_Conflicts.md#resolve_confirmed_time)|
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
|Derived From|[Sys_Resolved_Conflicts](Sys_Resolved_Conflicts.md).[Row_Version](Sys_Resolved_Conflicts.md#row_version)|
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


