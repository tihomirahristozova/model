# Table Gen_Printout_Layouts

Contains design layouts for document printouts. Entity: Gen_Printout_Layouts

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Printout_Layout_Id|`Guid`|`PK`, Readonly||
|Binary_Layout|`Byte[]`|`BLOB`|The printout layout, when the format requires binary storage. Alternative to Layout. |
|Document_Entity_Name|`String`||The entity name of the document type e.g. Crm_Sales_Orders, Inv_Store_Orders etc. `Required` `Filter(eq)` |
|Layout|`String`||The textual representation of the printout layout, when the format requires text representation. Alternative to Binary_Layout. |
|Layout_Format|`String`||Format specifier of the layout. Recognized by the application. `Required` `Filter(multi eq)` |
|Printout_Layout_Name|`String`||The name of this PrintoutLayout. `Required` `Filter(eq;like)` `ORD` |
|Notes|`String`||Notes for this PrintoutLayout. |
