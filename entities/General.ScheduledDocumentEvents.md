---
uid: General.ScheduledDocumentEvents
---
# General.ScheduledDocumentEvents

Contains postponed events, which will be executed later. Usually these are large number of recalculation events, resulting from other events. For example, releasing a cost correction, publishes postponed events for all affected documents. Entity: Gen_Scheduled_Document_Events

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.ScheduledDocumentEvents.md#Id) | guid |  
| [Cancelled](General.ScheduledDocumentEvents.md#Cancelled) | boolean | When true, specifies that this document event has been cancelled (either manually or in respect to another event) and will not be executed. [Required] [Default(false)] [Filter(eq)] 
| [CreationTime](General.ScheduledDocumentEvents.md#CreationTime) | datetime | Date and time when the ScheduledDocumentEvent was created. [Required] [Default(Now)] [ReadOnly] 
| [DocumentEvent](General.ScheduledDocumentEvents.md#DocumentEvent) | string | The type of the document event that is scheduled to be processed. [Required] [ReadOnly] 
| [LastProcessStatus](General.ScheduledDocumentEvents.md#LastProcessStatus) | string (nullable) | Status/information of the last attemp to process the event. Usually shows the cause in case of failure. [ReadOnly] 
| [LastProcessTime](General.ScheduledDocumentEvents.md#LastProcessTime) | datetime (nullable) | The time of the last attempt to process the event. [ReadOnly] 
| [Processed](General.ScheduledDocumentEvents.md#Processed) | boolean | Indicates wheather the event is already processed or not. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [State](General.ScheduledDocumentEvents.md#State) | [General.ScheduledDocumentEventsRepository.State](General.ScheduledDocumentEvents.md#State) | The state of the document for which the event will be processed. [Required] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](General.ScheduledDocumentEvents.md#Document) | [General.Documents](General.Documents.md) | The document for which the event will be processed. [Required] [Filter(multi eq)] [ReadOnly] |
| [SourceDocument](General.ScheduledDocumentEvents.md#SourceDocument) | [General.Documents](General.Documents.md) | The document that has caused this event to be scheduled. [Required] [Filter(multi eq)] [ReadOnly] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Cancelled

> When true, specifies that this document event has been cancelled (either manually or in respect to another event) and will not be executed. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### CreationTime

> Date and time when the ScheduledDocumentEvent was created. [Required] [Default(Now)] [ReadOnly]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### DocumentEvent

> The type of the document event that is scheduled to be processed. [Required] [ReadOnly]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LastProcessStatus

> Status/information of the last attemp to process the event. Usually shows the cause in case of failure. [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LastProcessTime

> The time of the last attempt to process the event. [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Processed

> Indicates wheather the event is already processed or not. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### State

> The state of the document for which the event will be processed. [Required] [ReadOnly]

_Type_: **[General.ScheduledDocumentEventsRepository.State](General.ScheduledDocumentEvents.md#State)**  
Allowed values for the [State](General.ScheduledDocumentEvents.md#State) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| New | New value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'New' |
| Corrective | Corrective value. Stored as 5. <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Corrective' |
| Planned | Planned value. Stored as 10. <br /> _Database Value:_ 10 <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Planned' |
| FirmPlanned | FirmPlanned value. Stored as 20. <br /> _Database Value:_ 20 <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'FirmPlanned' |
| Released | Released value. Stored as 30. <br /> _Database Value:_ 30 <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'Released' |
| Completed | Completed value. Stored as 40. <br /> _Database Value:_ 40 <br /> _Model Value:_ 40 <br /> _Domain API Value:_ 'Completed' |
| Closed | Closed value. Stored as 50. <br /> _Database Value:_ 50 <br /> _Model Value:_ 50 <br /> _Domain API Value:_ 'Closed' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Document

> The document for which the event will be processed. [Required] [Filter(multi eq)] [ReadOnly]

_Type_: **[General.Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SourceDocument

> The document that has caused this event to be scheduled. [Required] [Filter(multi eq)] [ReadOnly]

_Type_: **[General.Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.ScheduledDocumentEvents erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.ScheduledDocumentEvents erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.ScheduledDocumentEvents erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_ScheduledDocumentEvents?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_ScheduledDocumentEvents?$top=10>

