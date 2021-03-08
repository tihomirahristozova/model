# Table Acc_Template_Lines

Each template line contains the posting to a single set of debit and credit account. It also specifies the way to calculate the amount. Entity: Acc_Template_Lines

# Aggregate Hierarchy

* [Acc_Templates](Acc_Templates.md)
* [Wf_Routes](Wf_Routes.md)
* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Template_Line_Id|`Guid`|`PK`, Readonly||
|Amount_Column_Name|`String`||The name of the column within the amount rowset where the amount is located. `Required` |
|Amount_Condition|`AmountCondition?`|Allowed: `+`, `-`|Condition for the amount. The line is accounted only when the condition is matched. The condition can be one of: null - no condition, the line should be accounted unconditionally; '+' - The amount should be positive; '-' - The amount should be negative. The amount is matched as returned from the source, before applying the Multiplier. |
|Amount_Row_Id|`Guid?`||The id of the row from the amount rowset where the amount is located. null means to account one by one for all rows within the rowset. `Filter(multi eq)` |
|Amount_Row_Name|`String`||The name of definition, specified in Amount_Row_Id. null means that no Amount_Row_Id is specified or there is no name. |
|Amount_Source_Filter|`DataAccessFilter`||Filter that further specifies which rows from the amount rowset determine the amount. |
|Amount_Source_Name|`String`||The source rowset for the amount. For example: DocLines, DocHeader, Additional Amounts, Stock Types, etc. `Required` |
|Filter_XML|`DataAccessFilter`||The line is accounted only when the filter is satisfied compared with the source document header. |
|Line_No|`Int32`||Consecutive number of the line within the template. Determines the order of execution of the template lines. `Required` |
|Multiplier|`Decimal`||Factor by which the amount from the source will be multiplied. `Required` `Default(1)` |
|Notes|`String`||Notes for this TemplateLine. |
|Valid_From_Date|`DateTime?`||Start date from which the accounting template line is valid. `Filter(multi eq;ge;le)` |
|Valid_To_Date|`DateTime?`||End date to which the accounting template line is valid. `Filter(multi eq;ge;le)` |
