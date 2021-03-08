# Table Gen_Documents

Contains all documents issued by and to the enterprise. Entity: Gen_Documents

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly|Gets the Id of the document row, related to the domain object |
|Adjustment_Number|`Int32`|Readonly|Consecutive number of the correction that this document is applying to the adjusted document. `Required` `Default(0)` `ReadOnly` |
|Adjustment_Time|`DateTime?`|Readonly|Date/time when the document last has been adjusted by corrective document. `ReadOnly` |
|Adjustment_User|`String`|Readonly|The user who adjusted the document. `ReadOnly` |
|Complete_Time|`DateTime?`|Readonly|Date and time when the document was completed (State set to Completed). `Filter(ge;le)` `ReadOnly` |
|Creation_Time|`DateTime`|Readonly|Date/Time when the document was created. `Required` `Default(Now)` `Filter(ge;le)` `ReadOnly` |
|Creation_User|`String`|Readonly|The login name of the user, who created the document. `Required` `Filter(like)` `ReadOnly` |
|Document_Date|`DateTime`||The date on which the document was issued. `Required` `Default(Today)` `Filter(eq;ge;le)` `ORD` |
|Document_No|`String`||Document number, unique within Document_Type_Id. `Required` `Filter(eq;like)` `ORD` |
|Notes|`String`||Notes for this Document. |
|Document_Version|`Int32`|Readonly|Consecutive version number, starting with 1. Each update produces a new version of the document. `Required` `Default(1)` `Filter(eq;ge;le)` `ReadOnly` |
|Entity_Name|`String`|Readonly|The entity name of the document header. `Required` `Filter(eq)` `ORD` `ReadOnly` |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType?`|Allowed: `S`, `N`, Readonly|Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. `ReadOnly` |
|Planning_Only|`Boolean`|Readonly|Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned). `Required` `Default(false)` `ReadOnly` |
|Read_Only|`Boolean`|Readonly|True - the document is read only; false - the document is not read only. `Required` `Default(false)` `ReadOnly` |
|Reference_Date|`DateTime?`||The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken. `Default(Today)` `Filter(ge;le)` |
|Reference_Document_No|`String`||The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents. `Filter(eq;like)` |
|Release_Time|`DateTime?`|Readonly|Date and time when the document was released (State set to Released). `Filter(ge;le)` `ReadOnly` |
|State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly|The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed. `Required` `Default(0)` `Filter(multi eq;ge;le)` `ReadOnly` |
|Void|`Boolean`|Readonly|True if the document is null and void. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Void_Reason|`String`|Readonly|Reason for voiding the document, entered by the user. `ReadOnly` |
|Void_Time|`DateTime?`|Readonly|Date/time when the document has become void. `ReadOnly` |
|Void_User|`String`|Readonly|The user who voided the document. `ReadOnly` |
