# Table Gen_Printouts

Contains data about binding of printout layouts to specific user-defined document types. Entity: Gen_Printouts

# Aggregate Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Printout_Id|`Guid`|`PK`, Readonly||
|Allow_Printing_On_State|`AllowPrintingOnState`|Allowed: `0`, `10`, `20`, `30`, `40`, `50`|The user can print documents only with state equal or greater than Allow_Printing_On_State. `Required` `Default(0)` |
|Application_Name|`String`||The application which stored and uses the printout. `Required` |
|Backward_Compatibility|`Boolean`||Obsolete. Not used. `Required` `Default(false)` |
|Copies|`Int32`||Number of copies that should be printed when using direct printing. `Required` `Default(1)` |
|Definition|`String`||Obsolete. Not used. |
|Definition_Format|`String`||Obsolete. Not used. `Default("default")` |
|Is_Default|`Boolean`||True if this is the default printout for the application form. `Required` `Default(false)` `Filter(eq)` |
|Printout_Name|`String`||The name of the printout. Unique within the application form. `Required` `Filter(like)` |
|Notes|`String`||Notes for this Printout. |
|Ord|`Int32`||Order in the list of printouts when using direct printing. `Required` `Default(0)` |
|Ord_Filter_Xml|`DataAccessFilter`||The condition, required to be matched in order for the printout to be executed upon "Print All" command. |
|Ord_Priority|`Int32?`||Ordinal position and priority of the printout, in regard to other printouts within the current document type. Used for sorting, when executing printouts with "Print All" command. `Default(0)` |
