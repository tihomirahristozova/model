# Table Sys_Translations

Contains user-defined translations for non-english languages of the user interface and program messages. Entity: Sys_Translations

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Translation_Id|`Guid`|`PK`, Readonly||
|Active|`Boolean`||True when the translation is verified and activated. `Required` `Default(true)` `Filter(eq)` |
|Application_Name|`String`||The application, containing the resource. For base resource types (T,C,H), this is null. `Filter(eq)` `ORD` |
|Creation_Time|`DateTime`|Readonly|Timestamp when the translation was first created. `Required` `Default(Now)` `Filter(ge;le)` `ReadOnly` |
|Language|`String`||The code of the language or language-culture pair. Standard Windows codes are used. English="en"; US English = "en-us". `Required` `Default("en")` `Filter(eq)` |
|Resource_Id|`String`||The unique identifier of the translated resource. Should use ASCII/English chars only. Shorter strings are suggested. Depending on Text_Type: T:TableName; C:ColumnName; H:TableName.ColumnName; E,M,S: Application specific code. `Required` `Filter(eq;like)` |
|Resource_Type|`ResourceType`|Allowed: `T`, `C`, `H`, `R`, `E`, `M`, `S`|T=Table (entity) Name; C=Column Name; H=Column Hint; R=Meta Resource; E=Error; M=Message; S=Other application specific String. `Required` `Default("S")` `Filter(eq)` |
|Translation|`String`||The translated text. `Required` |
|Update_Time|`DateTime`|Readonly|When the translation was last updated. `Required` `Default(Now)` `ReadOnly` |
