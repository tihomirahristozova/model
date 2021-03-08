# Table Sys_External_Applications

List of external applications. Used to run external applications. Entity: Sys_External_Applications

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|External_Application_Id|`Guid`|`PK`, Readonly||
|Address|`String`||The address (path) to the application. The address is platform-dependant. `Required` |
|Available_In_Mode|`AvailableInMode`|Allowed: `SINGLE`, `LIST`, `ALL`|Whether the application will be displayed to the end users when a single object is opened or when multiple objects are listed. `Required` `Default("SINGLE")` `Filter(eq)` |
|Entity_Name|`String`||The entity, for which the application is defined. `Required` `Filter(eq)` `ORD` |
|Execute_For_All_Objects|`Boolean`||Whether to execute the application for all selected objects at once or to execute the application for each object, one by one. `Required` `Default(true)` `Filter(eq)` |
|Is_Active|`Boolean`||Specifies whether the external application is currently used. `Default(true)` `Filter(eq)` |
|External_Application_Name|`MultilanguageString`||The name of the external application. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this ExternalApplication. |
|Platform|`Platform`|Allowed: `WINDOWS`, `WEBPAGE`, `WEBSERVICE`, `ANDROID`, `iOS`|The execution platform of the application. `Required` `Filter(eq)` |
|Refresh_After_Finish|`Boolean`||Whether to refresh the data, displayed to the user, after the execution finishes. Not all platforms and/or applications support finish notification. `Required` `Default(true)` `Filter(eq)` |
|Save_Before_Start|`Boolean`||Whether to save the form data to the server before starting the application. `Required` `Default(true)` `Filter(eq)` |
