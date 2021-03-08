# Table Gen_Coding_Systems

Coding systems categorize additional product codes. Entity: Gen_Coding_Systems

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Coding_System_Id|`Guid`|`PK`, Readonly||
|Description|`String`||The description of this CodingSystem. |
|Is_Unique|`Boolean`||True when the coding system can contain only unique product codes. false - duplicate product codes are allowed. `Required` `Default(true)` `Filter(eq)` |
|Coding_System_Name|`MultilanguageString`||The name of this CodingSystem. `Required` `Filter(eq;like)` |
