# Systems.Workflow.Processes

Contains the business process diagrams. Entity: Wf_Processes

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Workflow.Processes.md#Id) | guid |  
| [CreationTime](Systems.Workflow.Processes.md#CreationTime) | datetime (nullable) | Date and time when the Process was created. [ReadOnly] 
| [CreationUser](Systems.Workflow.Processes.md#CreationUser) | string (nullable) | Login name of the user, who created the Process. [ReadOnly] 
| [IsLandscape](Systems.Workflow.Processes.md#IsLandscape) | boolean | Specifies whether the process diagram is intended to be viewed in landscape mode. [Required] [Default(true)] 
| [Notes](Systems.Workflow.Processes.md#Notes) | string (nullable) | Notes for this Process. 
| [Name](Systems.Workflow.Processes.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | The name of this Process. [Required] [Filter(eq;like)] 
| [SchemaFormat](Systems.Workflow.Processes.md#SchemaFormat) | string | Application specific format of the Schema Layout. [Required] [Default("D")] 
| [SchemaLayout](Systems.Workflow.Processes.md#SchemaLayout) | string | Contains the actual presentation layout of the business process. The layout is stored in the format, specified by Schema Format. [Required] 
| [StartEvent](Systems.Workflow.Processes.md#StartEvent) | string (nullable) | USR=User created; EML=Email receive (still not supported). null means that there is no starting event for this process. 
| [StartRoleId](Systems.Workflow.Processes.md#StartRoleId) | guid (nullable) | When Start_Event='USR' then specifies the role which the user must play in order to start the process. null when Start_Event<>'USR'. [Filter(multi eq)] 
| [Thumbnail](Systems.Workflow.Processes.md#Thumbnail) | byte[] (nullable) | Contains the visual thumbnail of the presentation of the business process. It is stored in bitmap (BMP) format. 
| [UpdateTime](Systems.Workflow.Processes.md#UpdateTime) | datetime (nullable) | Date and time when the Process was last updated. [ReadOnly] 
| [UpdateUser](Systems.Workflow.Processes.md#UpdateUser) | string (nullable) | Login name of the user, who last updated the Process. [ReadOnly] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CreationTime

> Date and time when the Process was created. [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CreationUser

> Login name of the user, who created the Process. [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsLandscape

> Specifies whether the process diagram is intended to be viewed in landscape mode. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

> Notes for this Process.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> The name of this Process. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### SchemaFormat

> Application specific format of the Schema Layout. [Required] [Default("D")]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **D**  

### SchemaLayout

> Contains the actual presentation layout of the business process. The layout is stored in the format, specified by Schema Format. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartEvent

> USR=User created; EML=Email receive (still not supported). null means that there is no starting event for this process.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartRoleId

> When Start_Event='USR' then specifies the role which the user must play in order to start the process. null when Start_Event<>'USR'. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Thumbnail

> Contains the visual thumbnail of the presentation of the business process. It is stored in bitmap (BMP) format.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UpdateTime

> Date and time when the Process was last updated. [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UpdateUser

> Login name of the user, who last updated the Process. [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Workflow.Processes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Workflow.Processes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Workflow.Processes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Workflow_Processes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Workflow_Processes?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Wf_Processes?$top=10>

