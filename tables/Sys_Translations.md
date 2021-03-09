# Table Sys_Translations

Contains user-defined translations for non-english languages of the user interface and program messages. Entity: Sys_Translations

## Summary

| Name | Type | Description |
| - | - | --- |
|[Translation_Id](#translation_id)|`uniqueidentifier` `PK`||
|[Application_Name](#application_name)|`nvarchar(50)` |The application, containing the resource. For base resource types (T,C,H), this is NULL|
|[Language](#language)|`nvarchar(8)` |The code of the language or language-culture pair. Standard Windows codes are used. English="en"; US English = "en-us"|
|[Resource_Type](#resource_type)|`nvarchar(1)` Allowed: `T`, `C`, `H`, `R`, `E`, `M`, `S`|T=Table (entity) Name; C=Column Name; H=Column Hint; R=Meta Resource; E=Error; M=Message; S=Other application specific String|
|[Resource_Id](#resource_id)|`nvarchar(800)` |The unique identifier of the translated resource. Should use ASCII/English chars only. Shorter strings are suggested. Depending on Text_Type: T:TableName; C:ColumnName; H:TableName.ColumnName; E,M,S: Application specific code|
|[Translation](#translation)|`nvarchar(2147483647)` |The translated text|
|[Creation_Time](#creation_time)|`datetime` Readonly|Timestamp when the translation was first created|
|[Update_Time](#update_time)|`datetime` Readonly|When the translation was last updated|
|[Active](#active)|`bit` |True when the translation is verified and activated.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Translation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Application_Name

| Property | Value |
| - | - |
|Type|nvarchar(50)|

### Language

| Property | Value |
| - | - |
|Type|nvarchar(8)|

### Resource_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Resource_Id

| Property | Value |
| - | - |
|Type|nvarchar(800)|

### Translation

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


