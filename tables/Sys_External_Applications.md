# Table Sys_External_Applications

List of external applications. Used to run external applications. Entity: Sys_External_Applications

## Summary

| Name | Type | Description |
| - | - | --- |
|[External_Application_Id](#external_application_id)|`uniqueidentifier` `PK`||
|[Entity_Name](#entity_name)|`nvarchar(64)` |The entity, for which the application is defined.|
|[External_Application_Name](#external_application_name)|`nvarchar(254)` `ML`|The name of the external application.|
|[Platform](#platform)|`nvarchar(12)` Allowed: `WINDOWS`, `WEBPAGE`, `WEBSERVICE`, `ANDROID`, `iOS`|The execution platform of the application.|
|[Address](#address)|`nvarchar(2147483647)` |The address (path) to the application. The address is platform-dependant.|
|[Available_In_Mode](#available_in_mode)|`nvarchar(6)` Allowed: `SINGLE`, `LIST`, `ALL`|Whether the application will be displayed to the end users when a single object is opened or when multiple objects are listed.|
|[Execute_For_All_Objects](#execute_for_all_objects)|`bit` |Whether to execute the application for all selected objects at once or to execute the application for each object, one by one.|
|[Save_Before_Start](#save_before_start)|`bit` |Whether to save the form data to the server before starting the application.|
|[Refresh_After_Finish](#refresh_after_finish)|`bit` |Whether to refresh the data, displayed to the user, after the execution finishes. Not all platforms and/or applications support finish notification.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` ||
|[Is_Active](#is_active)|`bit` |Specifies whether the external application is currently used.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### External_Application_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### External_Application_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Platform

| Property | Value |
| - | - |
|Type|nvarchar(12)|

### Address

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Available_In_Mode

| Property | Value |
| - | - |
|Type|nvarchar(6)|

### Execute_For_All_Objects

| Property | Value |
| - | - |
|Type|bit|

### Save_Before_Start

| Property | Value |
| - | - |
|Type|bit|

### Refresh_After_Finish

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


