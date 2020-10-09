---
uid: Systems.Bpm.Processes
---
# Systems.Bpm.Processes Entity

Represents one business process version. All process model elements and execution instances are bound to specfic process version. Entity: Bpm_Processes

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Systems.Bpm.Processes.md#code) | string | Unique process code. [Required] [Filter(multi eq)] [ORD] 
| [Description](Systems.Bpm.Processes.md#description) | string (nullable) | The description of this Process. [Filter(eq;like)] 
| [Id](Systems.Bpm.Processes.md#id) | guid |  
| [IsExecutable](Systems.Bpm.Processes.md#isexecutable) | boolean | Specifies whether the process is executable. In order to be executable, a process must contain enough execution details. Note, that some processes are only for documentation purposes and are not intended to be executed. [Required] [Default(false)] [Filter(eq)] 
| [IsPublished](Systems.Bpm.Processes.md#ispublished) | boolean | Specifies whether the process is currently published for new instances. [Required] [Default(false)] [Filter(eq)] 
| [Locality](Systems.Bpm.Processes.md#locality) | [Locality](Systems.Bpm.Processes.md#locality) | Process execution locality. Represents where the execution takes place and influences the selection of possible executors. For example, when L, the execution is private to the location, where the process originated. P=Same as parent; L=Location; C=Company; I=Intra-company. [Required] [Default("L")] [Filter(like)] 
| [Name](Systems.Bpm.Processes.md#name) | string | The name of this Process. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProcessGroup](Systems.Bpm.Processes.md#processgroup) | [ProcessGroups](Systems.Bpm.ProcessGroups.md) | The process group, to which this process belongs. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Connections | [ProcessConnections](Systems.Bpm.ProcessConnections.md) | List of [ProcessConnection](Systems.Bpm.ProcessConnections.md) child objects, based on the [Systems.Bpm.ProcessConnection.Process](Systems.Bpm.ProcessConnections.md#process) back reference 
| Elements | [ProcessElements](Systems.Bpm.ProcessElements.md) | List of [ProcessElement](Systems.Bpm.ProcessElements.md) child objects, based on the [Systems.Bpm.ProcessElement.Process](Systems.Bpm.ProcessElements.md#process) back reference 
| Lanes | [ProcessLanes](Systems.Bpm.ProcessLanes.md) | List of [ProcessLane](Systems.Bpm.ProcessLanes.md) child objects, based on the [Systems.Bpm.ProcessLane.Process](Systems.Bpm.ProcessLanes.md#process) back reference 
| Nodes | [ProcessNodes](Systems.Bpm.ProcessNodes.md) | List of [ProcessNode](Systems.Bpm.ProcessNodes.md) child objects, based on the [Systems.Bpm.ProcessNode.Process](Systems.Bpm.ProcessNodes.md#process) back reference 


## Attribute Details

### Code

Unique process code. [Required] [Filter(multi eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **True**  

### Description

The description of this Process. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsExecutable

Specifies whether the process is executable. In order to be executable, a process must contain enough execution details. Note, that some processes are only for documentation purposes and are not intended to be executed. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsPublished

Specifies whether the process is currently published for new instances. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Locality

Process execution locality. Represents where the execution takes place and influences the selection of possible executors. For example, when L, the execution is private to the location, where the process originated. P=Same as parent; L=Location; C=Company; I=Intra-company. [Required] [Default("L")] [Filter(like)]

_Type_: **[Locality](Systems.Bpm.Processes.md#locality)**  
Generic enum type for Locality properties  
_Allowed Values (Systems.Bpm.Locality Enum Members)_  

| Value | Description |
| ---- | --- |
| Parent | Parent value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Parent' |
| Location | Location value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Location' |
| Company | Company value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Company' |
| IntraCompany | IntraCompany value. Stored as 'I'. <br /> _Database Value:_ 'I' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'IntraCompany' |

_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Default Value_: **Location**  

### Name

The name of this Process. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### ProcessGroup

The process group, to which this process belongs. [Required] [Filter(multi eq)]

_Type_: **[ProcessGroups](Systems.Bpm.ProcessGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Bpm.Processes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Bpm.Processes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_Processes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_Processes?$top=10>

