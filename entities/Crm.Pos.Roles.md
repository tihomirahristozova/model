---
uid: Crm.Pos.Roles
---
# Crm.Pos.Roles Entity

Represents a role, which can be assigned to POS operators (like Cashier, Manager, etc.). The role indicates the operations, which are allowed to be performed by the operators. Entity: Pos_Roles (Introduced in version 19.1)

Default Display Text Format:  
_{PosRoleCode}: {PosRoleName:T}_  
Default Search Member:  
_PosRoleCode_  

Aggregate Tree:  
* [Crm.Pos.Roles](Crm.Pos.Roles.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CanProcessMinusSales](Crm.Pos.Roles.md#canprocessminussales) | boolean | Indicates whether the role is allowed to process minus (qty and/or value) sales. [Required] [Default(false)] [Filter(multi eq)] 
| [CanVoidSales](Crm.Pos.Roles.md#canvoidsales) | boolean | Indicates whether this role can void sales orders. [Required] [Default(false)] [Filter(multi eq)] 
| [Id](Crm.Pos.Roles.md#id) | guid |  
| [PosRoleCode](Crm.Pos.Roles.md#posrolecode) | string | Unique role code. [Required] [Filter(multi eq;like)] [ORD] 
| [PosRoleName](Crm.Pos.Roles.md#posrolename) | [MultilanguageString](../data-types.md#multilanguagestring) | Multi-language name of the POS role. [Required] [Filter(multi eq;like)] 


## Attribute Details

### CanProcessMinusSales

Indicates whether the role is allowed to process minus (qty and/or value) sales. [Required] [Default(false)] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### CanVoidSales

Indicates whether this role can void sales orders. [Required] [Default(false)] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### PosRoleCode

Unique role code. [Required] [Filter(multi eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  

### PosRoleName

Multi-language name of the POS role. [Required] [Filter(multi eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Pos.Roles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Pos.Roles erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pos_Roles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pos_Roles?$top=10>

