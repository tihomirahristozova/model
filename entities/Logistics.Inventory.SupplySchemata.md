---
uid: Logistics.Inventory.SupplySchemata
---
# Logistics.Inventory.SupplySchemata Entity

**Namespace:** [Logistics.Inventory](Logistics.Inventory.md)  

Obsolete. Not used. Entity: Inv_Supply_Schemata

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Inventory.SupplySchemata](Logistics.Inventory.SupplySchemata.md)  
  * [Logistics.Inventory.SupplySchemaRoutes](Logistics.Inventory.SupplySchemaRoutes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.SupplySchemata.md#id) | guid |  
| [Name](Logistics.Inventory.SupplySchemata.md#name) | string (254) | The name of this SupplySchema. `Required` 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Routes | [SupplySchemaRoutes](Logistics.Inventory.SupplySchemaRoutes.md) | List of `SupplySchemaRoute`(Logistics.Inventory.SupplySchemaRoutes.md) child objects, based on the `Logistics.Inventory.SupplySchemaRoute.SupplySchema`(Logistics.Inventory.SupplySchemaRoutes.md#supplyschema) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this SupplySchema. `Required`

_Type_: **string (254)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  



## Business Rules

[!list erp.entity=Logistics.Inventory.SupplySchemata erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.SupplySchemata erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_SupplySchemata?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_SupplySchemata?$top=10>

