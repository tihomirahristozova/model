---
uid: Systems.Bpm.ProcessConnections
---
# Systems.Bpm.ProcessConnections

Contains the connections between process elements. Part of the process model. Entity: Bpm_Process_Connections

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Bpm.ProcessConnections.md#Id) | guid |  
| [ConditionFilterXml](Systems.Bpm.ProcessConnections.md#ConditionFilterXml) | dataaccessfilter (nullable) | When not null, specifies that the flow will be followed only if the condition is matched by the current values in the process instance. [Filter(eq;like)] 
| [IsDefault](Systems.Bpm.ProcessConnections.md#IsDefault) | boolean | Denotes this flow as the default sequence flow. It is taken only when all other flows are not valid. For example, gateways usually are followed by several conditional flows and one default flow. [Required] [Default(false)] [Filter(eq)] 
| [Code](Systems.Bpm.ProcessConnections.md#Code) | string | Connection code, unique within the process. Used as ID for XML serialization purposes. [Required] [Default(New Guid)] [Filter(eq;like)] 
| [Name](Systems.Bpm.ProcessConnections.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Multilanguage connection name. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Process](Systems.Bpm.ProcessConnections.md#Process) | [Systems.Bpm.Processes](Systems.Bpm.Processes.md) | The process version to which this connection belongs. [Required] [Filter(multi eq)] [Owner] |
| [SourceProcessNode](Systems.Bpm.ProcessConnections.md#SourceProcessNode) | [Systems.Bpm.ProcessNodes](Systems.Bpm.ProcessNodes.md) | The element, from which the connection starts. The element should be in the same process as the connection. [Required] [Filter(multi eq)] |
| [TargetProcessNode](Systems.Bpm.ProcessConnections.md#TargetProcessNode) | [Systems.Bpm.ProcessNodes](Systems.Bpm.ProcessNodes.md) | The element, at which the connection ends. The element should be in the same process as the connection. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ConditionFilterXml

> When not null, specifies that the flow will be followed only if the condition is matched by the current values in the process instance. [Filter(eq;like)]

_Type_: **dataaccessfilter (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### IsDefault

> Denotes this flow as the default sequence flow. It is taken only when all other flows are not valid. For example, gateways usually are followed by several conditional flows and one default flow. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Code

> Connection code, unique within the process. Used as ID for XML serialization purposes. [Required] [Default(New Guid)] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Name

> Multilanguage connection name. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### Process

> The process version to which this connection belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Bpm.Processes](Systems.Bpm.Processes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SourceProcessNode

> The element, from which the connection starts. The element should be in the same process as the connection. [Required] [Filter(multi eq)]

_Type_: **[Systems.Bpm.ProcessNodes](Systems.Bpm.ProcessNodes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TargetProcessNode

> The element, at which the connection ends. The element should be in the same process as the connection. [Required] [Filter(multi eq)]

_Type_: **[Systems.Bpm.ProcessNodes](Systems.Bpm.ProcessNodes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Bpm.ProcessConnections erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Bpm.ProcessConnections erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Bpm.ProcessConnections erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_ProcessConnections?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_ProcessConnections?$top=10>

