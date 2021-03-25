---
uid: Logistics.Inventory.ScrapTypes
---
# Logistics.Inventory.ScrapTypes Entity

**Namespace:** [Logistics.Inventory](Logistics.Inventory.md)  

Types of scrap. Used in store transactions to categorize scrap, when it occurs. Entity: Inv_Scrap_Types

## Default Visualization
Default Display Text Format:  
_{Id}_  
Default Search Member:  
_Id_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Inventory.ScrapTypes](Logistics.Inventory.ScrapTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](Logistics.Inventory.ScrapTypes.md#description) | string(254) (nullable) | The description of this ScrapType. `Filter(like)` 
| [Id](Logistics.Inventory.ScrapTypes.md#id) | guid |  
| [IsPlanned](Logistics.Inventory.ScrapTypes.md#isplanned) | boolean | True=Planned (expected) scrap. Scrap of this type will be used to refine planned scrap for future operations. 2=Unexpected scrap. `Required` `Default(true)` `Filter(eq)` 


## Attribute Details

### Description

The description of this ScrapType. `Filter(like)`

_Type_: **string(254) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsPlanned

True=Planned (expected) scrap. Scrap of this type will be used to refine planned scrap for future operations. 2=Unexpected scrap. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  



## Business Rules

[!list erp.entity=Logistics.Inventory.ScrapTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.ScrapTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_ScrapTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_ScrapTypes?$top=10>

