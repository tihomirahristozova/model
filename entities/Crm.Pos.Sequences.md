---
uid: Crm.Pos.Sequences
---
# Crm.Pos.Sequences

Stores the last issued fiscal sales number for each POS device. Entity: Pos_Sequences (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Pos.Sequences.md#Id) | guid |  
| [IsActive](Crm.Pos.Sequences.md#IsActive) | boolean | Indicates whether this sequence is active. [Required] [Default(true)] [Filter(multi eq)] 
| [MaxNo](Crm.Pos.Sequences.md#MaxNo) | string (nullable) | Specifies the maximum number allowed in the sequence. null means that the sequence will grow unlimited. [Filter(multi eq;ge;le)] 
| [NextNo](Crm.Pos.Sequences.md#NextNo) | string | The next consecutive number which will be assigned on the next request. [Required] [Filter(multi eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PosDevice](Crm.Pos.Sequences.md#PosDevice) | [Crm.Pos.Devices](Crm.Pos.Devices.md) | The POS device, for which the sequence is defined. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### IsActive

> Indicates whether this sequence is active. [Required] [Default(true)] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### MaxNo

> Specifies the maximum number allowed in the sequence. null means that the sequence will grow unlimited. [Filter(multi eq;ge;le)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

### NextNo

> The next consecutive number which will be assigned on the next request. [Required] [Filter(multi eq;ge;le)]

_Type_: **string**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### PosDevice

> The POS device, for which the sequence is defined. [Required] [Filter(multi eq)]

_Type_: **[Crm.Pos.Devices](Crm.Pos.Devices.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Pos.Sequences erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Pos.Sequences erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Pos.Sequences erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pos_Sequences?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pos_Sequences?$top=10>

