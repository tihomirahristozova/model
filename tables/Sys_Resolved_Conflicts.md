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

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### URL

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Table_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Conflict_Description

| Property | Value |
| - | - |
|Type|nvarchar(400)|

### Resolve_Description

| Property | Value |
| - | - |
|Type|nvarchar(400)|

### Resolved_Time

| Property | Value |
| - | - |
|Type|datetime|

### Revised_By_User

| Property | Value |
| - | - |
|Type|bit|

### Resolve_Confirmed_By_User

| Property | Value |
| - | - |
|Type|bit|

### Resolve_Confirmed_Time

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


