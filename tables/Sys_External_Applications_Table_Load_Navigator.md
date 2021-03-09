# Query Sys_External_Applications_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[External_Application_Id](#external_application_id)|`uniqueidentifier` `PK`||
|[Entity_Name](#entity_name)|`nvarchar` |The entity, for which the application is defined.|
|[External_Application_Name](#external_application_name)|`nvarchar` `ML`|The name of the external application.|
|[Platform](#platform)|`nvarchar` Allowed: `WINDOWS`, `WEBPAGE`, `WEBSERVICE`, `ANDROID`, `iOS`|The execution platform of the application.|
|[Address](#address)|`nvarchar` |The address (path) to the application. The address is platform-dependant.|
|[Available_In_Mode](#available_in_mode)|`nvarchar` Allowed: `SINGLE`, `LIST`, `ALL`|Whether the application will be displayed to the end users when a single object is opened or when multiple objects are listed.|
|[Execute_For_All_Objects](#execute_for_all_objects)|`bit` |Whether to execute the application for all selected objects at once or to execute the application for each object, one by one.|
|[Save_Before_Start](#save_before_start)|`bit` |Whether to save the form data to the server before starting the application.|
|[Refresh_After_Finish](#refresh_after_finish)|`bit` |Whether to refresh the data, displayed to the user, after the execution finishes. Not all platforms and/or applications support finish notification.|
|[Notes](#notes)|`nvarchar` ||
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` ||
|[Is_Active](#is_active)|`bit` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### External_Application_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### External_Application_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Platform

| Property | Value |
| - | - |
|Type|nvarchar|

### Address

| Property | Value |
| - | - |
|Type|nvarchar|

### Available_In_Mode

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

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


