# Table Acc_Template_Line_Properties

Contains the way to obtain the values for each required property of both the debit and the credit accounts. Entity: Acc_Template_Line_Properties

# Aggregate Hierarchy

* [Acc_Template_Lines](Acc_Template_Lines.md)
* [Acc_Templates](Acc_Templates.md)
* [Wf_Routes](Wf_Routes.md)
* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Template_Line_Property_Id|`Guid`|`PK`, Readonly||
|Constant_Value_Id|`Guid?`||The internal Id of a property value, selected as constant value. Applicable only when Property Value Source Type = Constant. `Filter(multi eq)` |
|Is_Debit|`Boolean`||If Is_Debit=true then this property is for the debit account in the template line for which is this record. If Is_Debit=false then the property is for the credit account. `Required` `Default(true)` `Filter(eq)` |
|Property_Description|`MultilanguageString`||Description for the property value that should be used when the description can't be determined by the source (e.g. when the source type is constant). |
|Property_No|`Int32`||The ordinal position of the property value in the item key of the account. `Required` `Filter(eq)` |
|Property_Value_Source|`String`||Source for the property value according to the chosen source type. `Required` |
|Property_Value_Source_Type|`String`||Type of source for the property value. For example: System properties, User properties for document, Constant, ... `Required` |
