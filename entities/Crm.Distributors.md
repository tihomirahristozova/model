---
uid: Crm.Distributors
---
# Crm.Distributors Entity

**Namespace:** [Crm](Crm.md)  

Distributors are external for the enterprise persons or companies who obtain sales orders from end-customers in benefit of the enterprise. Entity: Crm_Distributors

## Default Visualization
Default Display Text Format:  
_{Party.PartyCode}: {Party.PartyName:T}_  
Default Search Member:  
_Party.PartyCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Contacts.Parties](General.Contacts.Parties.md)  
Aggregate Root:  
[General.Contacts.Parties](General.Contacts.Parties.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FlatCommisionPercentage](Crm.Distributors.md#flatcommisionpercentage) | decimal (7, 6) | Not-zero if commision percentage should be applyied to all sales, regardless of product/discount/progressi<br />ve/qunatity considerations. `Required` `Default(0)` 
| [Id](Crm.Distributors.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Party](Crm.Distributors.md#party) | [Parties](General.Contacts.Parties.md) | Base party Id. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### FlatCommisionPercentage

Not-zero if commision percentage should be applyied to all sales, regardless of product/discount/progressive/qunatity considerations. `Required` `Default(0)`

_Type_: **decimal (7, 6)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Party

Base party Id. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Distributors erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Distributors erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Distributors?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Distributors?$top=10>

