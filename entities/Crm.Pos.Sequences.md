---
uid: Crm.Pos.Sequences
---
# Crm.Pos.Sequences Entity

**Namespace:** [Crm.Pos](Crm.Pos.md)  

Stores the last issued fiscal sales number for each POS device. Entity: Pos_Sequences (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{Id}_  
Default Search Member:  
_Id_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.Pos.Sequences](Crm.Pos.Sequences.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Pos.Sequences.md#id) | guid |  
| [IsActive](Crm.Pos.Sequences.md#isactive) | boolean | Indicates whether this sequence is active. `Required` `Default(true)` `Filter(multi eq)` 
| [MaxNo](Crm.Pos.Sequences.md#maxno) | string(16) (nullable) | Specifies the maximum number allowed in the sequence. null means that the sequence will grow unlimited. `Filter(multi eq;ge;le)` 
| [NextNo](Crm.Pos.Sequences.md#nextno) | string(16) | The next consecutive number which will be assigned on the next request. `Required` `Filter(multi eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PosDevice](Crm.Pos.Sequences.md#posdevice) | [Devices](Crm.Pos.Devices.md) | The POS device, for which the sequence is defined. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Indicates whether this sequence is active. `Required` `Default(true)` `Filter(multi eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### MaxNo

Specifies the maximum number allowed in the sequence. null means that the sequence will grow unlimited. `Filter(multi eq;ge;le)`

_Type_: **string(16) (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### NextNo

The next consecutive number which will be assigned on the next request. `Required` `Filter(multi eq;ge;le)`

_Type_: **string(16)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  


## Reference Details

### PosDevice

The POS device, for which the sequence is defined. `Required` `Filter(multi eq)`

_Type_: **[Devices](Crm.Pos.Devices.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Pos.Sequences erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Pos.Sequences erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pos_Sequences?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pos_Sequences?$top=10>

