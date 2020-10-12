---
uid: Systems.Workflow.Processes
---
# Systems.Workflow.Processes Entity

Contains the business process diagrams. Entity: Wf_Processes

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationTime](Systems.Workflow.Processes.md#creationtime) | datetime (nullable) | Date and time when the Process was created. [ReadOnly] 
| [CreationUser](Systems.Workflow.Processes.md#creationuser) | string (nullable) | Login name of the user, who created the Process. [ReadOnly] 
| [Id](Systems.Workflow.Processes.md#id) | guid |  
| [IsLandscape](Systems.Workflow.Processes.md#islandscape) | boolean | Specifies whether the process diagram is intended to be viewed in landscape mode. [Required] [Default(true)] 
| [Name](Systems.Workflow.Processes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this Process. [Required] [Filter(eq;like)] 
| [Notes](Systems.Workflow.Processes.md#notes) | string (nullable) | Notes for this Process. 
| [SchemaFormat](Systems.Workflow.Processes.md#schemaformat) | string | Application specific format of the Schema Layout. [Required] [Default("D")] 
| [SchemaLayout](Systems.Workflow.Processes.md#schemalayout) | string | Contains the actual presentation layout of the business process. The layout is stored in the format, specified by Schema Format. [Required] 
| [StartEvent](Systems.Workflow.Processes.md#startevent) | string (nullable) | USR=User created; EML=Email receive (still not supported). null means that there is no starting event for this process. 
| [StartRoleId](Systems.Workflow.Processes.md#startroleid) | guid (nullable) | When Start_Event='USR' then specifies the role which the user must play in order to start the process. null when Start_Event<>'USR'. [Filter(multi eq)] 
| [Thumbnail](Systems.Workflow.Processes.md#thumbnail) | byte[] (nullable) | Contains the visual thumbnail of the presentation of the business process. It is stored in bitmap (BMP) format. 
| [UpdateTime](Systems.Workflow.Processes.md#updatetime) | datetime (nullable) | Date and time when the Process was last updated. [ReadOnly] 
| [UpdateUser](Systems.Workflow.Processes.md#updateuser) | string (nullable) | Login name of the user, who last updated the Process. [ReadOnly] 


## Attribute Details

### CreationTime

Date and time when the Process was created. [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CreationUser

Login name of the user, who created the Process. [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsLandscape

Specifies whether the process diagram is intended to be viewed in landscape mode. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

The name of this Process. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this Process.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SchemaFormat

Application specific format of the Schema Layout. [Required] [Default("D")]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **D**  

### SchemaLayout

Contains the actual presentation layout of the business process. The layout is stored in the format, specified by Schema Format. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartEvent

USR=User created; EML=Email receive (still not supported). null means that there is no starting event for this process.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartRoleId

When Start_Event='USR' then specifies the role which the user must play in order to start the process. null when Start_Event<>'USR'. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Thumbnail

Contains the visual thumbnail of the presentation of the business process. It is stored in bitmap (BMP) format.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UpdateTime

Date and time when the Process was last updated. [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UpdateUser

Login name of the user, who last updated the Process. [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Workflow.Processes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Workflow.Processes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Workflow_Processes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Workflow_Processes?$top=10>

