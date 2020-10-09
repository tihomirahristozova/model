---
uid: General.Config
---
# General.Config Entity

Hierarchical repository of configuration options. Entity: Gen_Config

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](General.Config.md#description) | string (nullable) | The description of this Config. 
| [Id](General.Config.md#id) | guid |  
| [IsActive](General.Config.md#isactive) | boolean | Indicates whether this config entry is active. Inactive config entries are not taken into account. [Required] [Default(true)] [Filter(eq)] (Introduced in version 19.1) 
| [KeyPath](General.Config.md#keypath) | string | Full path of the configuration option. [Required] [Filter(eq)] [ORD] 
| [KeyValue](General.Config.md#keyvalue) | string (nullable) | The value of the configuration option. 
| [UserLogin](General.Config.md#userlogin) | string (nullable) | If not null, the configuration option is specific to the user. [Filter(eq)] 
| [UserMachine](General.Config.md#usermachine) | string (nullable) | If not null, the configuration option is specific to the machine. [Filter(eq)] 


## Attribute Details

### Description

The description of this Config.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Indicates whether this config entry is active. Inactive config entries are not taken into account. [Required] [Default(true)] [Filter(eq)] (Introduced in version 19.1)

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### KeyPath

Full path of the configuration option. [Required] [Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### KeyValue

The value of the configuration option.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UserLogin

If not null, the configuration option is specific to the user. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### UserMachine

If not null, the configuration option is specific to the machine. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Config erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Config erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Config erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Config?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Config?$top=10>

