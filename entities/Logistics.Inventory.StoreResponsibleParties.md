---
uid: Logistics.Inventory.StoreResponsibleParties
---
# Logistics.Inventory.StoreResponsibleParties Entity

**Namespace:** [Logistics.Inventory](Logistics.Inventory.md)  

Contains the list of responsible parties (usually persons) for the stores. Stores can have multiple responsible parties. Entity: Inv_Store_Responsible_Parties

## Default Visualization
Default Display Text Format:  
_{Store.PartyName:T} #{Store.PartyCode}_  
Default Search Member:  
_Store.PartyName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md)  
Aggregate Root:  
[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.StoreResponsibleParties.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ResponsibleParty](Logistics.Inventory.StoreResponsibleParties.md#responsibleparty) | [Parties](General.Contacts.Parties.md) | The responsible party (usually employee) of the store. `Required` `Filter(multi eq)` |
| [Store](Logistics.Inventory.StoreResponsibleParties.md#store) | [Stores](Logistics.Inventory.Stores.md) | The store for which we specify the responsible party. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### ResponsibleParty

The responsible party (usually employee) of the store. `Required` `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

The store for which we specify the responsible party. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Logistics.Inventory.StoreResponsibleParties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Inventory.StoreResponsibleParties erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_StoreResponsibleParties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_StoreResponsibleParties?$top=10>

