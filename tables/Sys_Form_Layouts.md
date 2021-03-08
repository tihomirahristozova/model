# Table Sys_Form_Layouts

Contains user layouts of the screen forms. Entity: Sys_Form_Layouts

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Form_Layout_Id|`Guid`|`PK`, Readonly||
|Application_Name|`String`||The application, which consumes the layout. `Required` `Filter(eq)` `ORD` |
|Form_Name|`String`||The form, for which the layout is applied. `Required` `Filter(eq;like)` |
|Layout|`Byte[]`|`BLOB`|The byte storage of the layout. |
|Layout_Format|`LayoutFormat`|Allowed: `D`, `L`, `U`|The format of the data in the Layout column. Values can be: 'U' - uncompressed; 'L' - LZO compressed; 'D' - Deflate compressed. `Required` `Default("U")` |
|Layout_Name|`String`||The name of a named layout. Standard layouts have empty string names. `Required` `Filter(eq;like)` |
|Panel_Name|`String`||The visual panel, for which the layout is applied. `Required` `Default("Form")` `Filter(eq)` |
|User_Name|`String`||The user for which the layout is applied. null means that the layout is applied for all users. `Filter(eq;like)` |
