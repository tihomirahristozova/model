# Systems.Bpm.ProcessElements

Contains the flow elements of the process model. Entity: Bpm_Process_Elements

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Bpm.ProcessElements.md#Id) | guid |  
| [ElementSubtype](Systems.Bpm.ProcessElements.md#ElementSubtype) | [Systems.Bpm.ProcessElementsRepository.ElementSubtype](Systems.Bpm.ProcessElements.md#ElementSubtype) | Subtype of the element. Each type allows only certain types of sub-types. [Required] [Filter(eq;like)] 
| [ElementType](Systems.Bpm.ProcessElements.md#ElementType) | [Systems.Bpm.ProcessElementsRepository.ElementType](Systems.Bpm.ProcessElements.md#ElementType) | Basic type of the element. A=Activity; E=Event; G=Gateway; C=Artifact. [Required] [Filter(eq;like)] 
| [InstructionsHtml](Systems.Bpm.ProcessElements.md#InstructionsHtml) | string (nullable) | Detailed instructions to the executor in HTML format. [Filter(eq;like)] 
| [Code](Systems.Bpm.ProcessElements.md#Code) | string | Element code, unique within the process. Used as ID for XML serialization purposes. [Required] [Filter(eq;like)] 
| [Name](Systems.Bpm.ProcessElements.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | Multilanguage process name. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Process](Systems.Bpm.ProcessElements.md#Process) | [Systems.Bpm.Processes](Systems.Bpm.Processes.md) | The process, to which this element belongs. [Required] [Filter(multi eq)] [Owner] |
| [ProcessLane](Systems.Bpm.ProcessElements.md#ProcessLane) | [Systems.Bpm.ProcessLanes](Systems.Bpm.ProcessLanes.md) | The process lane to which this element belongs. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ElementSubtype

> Subtype of the element. Each type allows only certain types of sub-types. [Required] [Filter(eq;like)]

_Type_: **[Systems.Bpm.ProcessElementsRepository.ElementSubtype](Systems.Bpm.ProcessElements.md#ElementSubtype)**  
Allowed values for the [ElementSubtype](Systems.Bpm.ProcessElements.md#ElementSubtype) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| ActivityUserTask | ActivityUserTask value. Stored as 'ATU'. <br /> _Database Value:_ 'ATU' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'ActivityUserTask' |
| ActivityManualTask | ActivityManualTask value. Stored as 'ATM'. <br /> _Database Value:_ 'ATM' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'ActivityManualTask' |
| ActivityServiceTask | ActivityServiceTask value. Stored as 'ATV'. <br /> _Database Value:_ 'ATV' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'ActivityServiceTask' |
| ActivityScriptTask | ActivityScriptTask value. Stored as 'ATC'. <br /> _Database Value:_ 'ATC' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'ActivityScriptTask' |
| ActivityBusinessRuleTask | ActivityBusinessRuleTask value. Stored as 'ATB'. <br /> _Database Value:_ 'ATB' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'ActivityBusinessRuleTask' |
| ActivitySendTask | ActivitySendTask value. Stored as 'ATS'. <br /> _Database Value:_ 'ATS' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'ActivitySendTask' |
| ActivityReceiveTask | ActivityReceiveTask value. Stored as 'ATR'. <br /> _Database Value:_ 'ATR' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'ActivityReceiveTask' |
| StartEvent | StartEvent value. Stored as 'ES1'. <br /> _Database Value:_ 'ES1' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'StartEvent' |
| StartEventMessage | StartEventMessage value. Stored as 'ES2'. <br /> _Database Value:_ 'ES2' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'StartEventMessage' |
| StartEventTimer | StartEventTimer value. Stored as 'ES4'. <br /> _Database Value:_ 'ES4' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'StartEventTimer' |
| EndEvent | EndEvent value. Stored as 'EE1'. <br /> _Database Value:_ 'EE1' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'EndEvent' |
| EndEventMessage | EndEventMessage value. Stored as 'EE2'. <br /> _Database Value:_ 'EE2' <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'EndEventMessage' |
| EndEventError | EndEventError value. Stored as 'EE5'. <br /> _Database Value:_ 'EE5' <br /> _Model Value:_ 12 <br /> _Domain API Value:_ 'EndEventError' |
| EndEventTerminate | EndEventTerminate value. Stored as 'EE9'. <br /> _Database Value:_ 'EE9' <br /> _Model Value:_ 13 <br /> _Domain API Value:_ 'EndEventTerminate' |
| IntermediateEventThrow | IntermediateEventThrow value. Stored as 'EI1'. <br /> _Database Value:_ 'EI1' <br /> _Model Value:_ 14 <br /> _Domain API Value:_ 'IntermediateEventThrow' |
| IntermediateEventThrowMessage | IntermediateEventThrowMessage value. Stored as 'EI2'. <br /> _Database Value:_ 'EI2' <br /> _Model Value:_ 15 <br /> _Domain API Value:_ 'IntermediateEventThrowMessage' |
| IntermediateEventCatchMessage | IntermediateEventCatchMessage value. Stored as 'EI3'. <br /> _Database Value:_ 'EI3' <br /> _Model Value:_ 16 <br /> _Domain API Value:_ 'IntermediateEventCatchMessage' |
| IntermediateEventCatchTimer | IntermediateEventCatchTimer value. Stored as 'EI4'. <br /> _Database Value:_ 'EI4' <br /> _Model Value:_ 17 <br /> _Domain API Value:_ 'IntermediateEventCatchTimer' |
| GatewayExclusive | GatewayExclusive value. Stored as 'GEX'. <br /> _Database Value:_ 'GEX' <br /> _Model Value:_ 18 <br /> _Domain API Value:_ 'GatewayExclusive' |
| GatewayInclusive | GatewayInclusive value. Stored as 'GIN'. <br /> _Database Value:_ 'GIN' <br /> _Model Value:_ 19 <br /> _Domain API Value:_ 'GatewayInclusive' |
| ArtifactTextAnnotation | ArtifactTextAnnotation value. Stored as 'CAT'. <br /> _Database Value:_ 'CAT' <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'ArtifactTextAnnotation' |
| ArtifactGroup | ArtifactGroup value. Stored as 'CGP'. <br /> _Database Value:_ 'CGP' <br /> _Model Value:_ 21 <br /> _Domain API Value:_ 'ArtifactGroup' |

_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ElementType

> Basic type of the element. A=Activity; E=Event; G=Gateway; C=Artifact. [Required] [Filter(eq;like)]

_Type_: **[Systems.Bpm.ProcessElementsRepository.ElementType](Systems.Bpm.ProcessElements.md#ElementType)**  
Allowed values for the [ElementType](Systems.Bpm.ProcessElements.md#ElementType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Activity | Activity value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Activity' |
| Event | Event value. Stored as 'E'. <br /> _Database Value:_ 'E' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Event' |
| Gateway | Gateway value. Stored as 'G'. <br /> _Database Value:_ 'G' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Gateway' |
| Artifact | Artifact value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Artifact' |

_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### InstructionsHtml

> Detailed instructions to the executor in HTML format. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Code

> Element code, unique within the process. Used as ID for XML serialization purposes. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Name

> Multilanguage process name. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### Process

> The process, to which this element belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Bpm.Processes](Systems.Bpm.Processes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProcessLane

> The process lane to which this element belongs. [Required] [Filter(multi eq)]

_Type_: **[Systems.Bpm.ProcessLanes](Systems.Bpm.ProcessLanes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Bpm.ProcessElements erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Bpm.ProcessElements erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Bpm.ProcessElements erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_ProcessElements?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_ProcessElements?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Bpm_Process_Elements?$top=10>

