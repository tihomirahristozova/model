# Table Bpm_Process_Elements

Contains the flow elements of the process model. Entity: Bpm_Process_Elements

# Aggregate Hierarchy

* [Bpm_Processes](Bpm_Processes.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Process_Element_Id|`Guid`|`PK`, Readonly||
|Process_Element_Code|`String`||Element code, unique within the process. Used as ID for XML serialization purposes. `Required` `Filter(eq;like)` |
|Element_Subtype|`ElementSubtype`|Allowed: `ATU`, `ATM`, `ATV`, `ATC`, `ATB`, `ATS`, `ATR`, `ES1`, `ES2`, `ES4`, `EE1`, `EE2`, `EE5`, `EE9`, `EI1`, `EI2`, `EI3`, `EI4`, `GEX`, `GIN`, `CAT`, `CGP`|Subtype of the element. Each type allows only certain types of sub-types. `Required` `Filter(eq;like)` |
|Element_Type|`ElementType`|Allowed: `A`, `E`, `G`, `C`|Basic type of the element. A=Activity; E=Event; G=Gateway; C=Artifact. `Required` `Filter(eq;like)` |
|Instructions_Html|`String`||Detailed instructions to the executor in HTML format. `Filter(eq;like)` |
|Process_Element_Name|`MultilanguageString`||Multilanguage process name. `Required` `Filter(eq;like)` |
