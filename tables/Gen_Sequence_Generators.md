# Table Gen_Sequence_Generators

Contains one or more sequence generators for each sequence. Many sequence generators for one sequence are used when the generators must be selected conditionally or when more generators are needed for parallel numbering. Entity: Gen_Sequence_Generators

# Aggregate Hierarchy

* [Gen_Sequences](Gen_Sequences.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Sequence_Generator_Id|`Guid`|`PK`, Readonly||
|Allow_Explicit_Numbering|`Boolean`||Allows to assign numbers explicitely regardless of the Next_Value of the generator (Next_Value is updated if needed). `Required` `Default(false)` |
|Next_Value|`String`||The next number that will be issued by the sequence. `Required` `Default("0000000001")` |
|Sequence_Priority|`Int32`||The priority in which the sequence is used, compared to other similar sequences. Used only for sequences, for which Simultaneous Transactions=True. `Required` `Default(1)` |
