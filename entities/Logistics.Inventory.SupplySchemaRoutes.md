---
uid: Logistics.Inventory.SupplySchemaRoutes
---
# Logistics.Inventory.SupplySchemaRoutes Entity

**Namespace:** [Logistics.Inventory](Logistics.Inventory.md)  

Obsolete. Not used. Entity: Inv_Supply_Schema_Routes

## Default Visualization
Default Display Text Format:  
_{SupplySchema.Name:T}_  
Default Search Member:  
_SupplySchema.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Inventory.SupplySchemata](Logistics.Inventory.SupplySchemata.md)  
Aggregate Root:  
[Logistics.Inventory.SupplySchemata](Logistics.Inventory.SupplySchemata.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.SupplySchemaRoutes.md#id) | guid |  
| [Notes](Logistics.Inventory.SupplySchemaRoutes.md#notes) | string (254) __nullable__ | Notes for this SupplySchemaRoute. 
| [SchemaXML](Logistics.Inventory.SupplySchemaRoutes.md#schemaxml) | string (1073741823) __nullable__ | Obsolete. Not used. (Used by the schematic control). 
| [TransitTimeDays](Logistics.Inventory.SupplySchemaRoutes.md#transittimedays) | int32 | Obsolete. Not used. (Time needed for the delivery of the goods using this route). `Required` `Default(0)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DestinationStore](Logistics.Inventory.SupplySchemaRoutes.md#destinationstore) | [Stores](Logistics.Inventory.Stores.md) | Obsolete. Not used. `Required` `Filter(multi eq)` |
| [SourceStore](Logistics.Inventory.SupplySchemaRoutes.md#sourcestore) | [Stores](Logistics.Inventory.Stores.md) | Obsolete. Not used. `Required` `Filter(multi eq)` |
| [SupplySchema](Logistics.Inventory.SupplySchemaRoutes.md#supplyschema) | [SupplySchemata](Logistics.Inventory.SupplySchemata.md) | The `SupplySchema`(Logistics.Inventory.SupplySchemaRoutes.md#supplyschema) to which this SupplySchemaRoute belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this SupplySchemaRoute.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### SchemaXML

Obsolete. Not used. (Used by the schematic control).

_Type_: **string (1073741823) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **1073741823**  

### TransitTimeDays

Obsolete. Not used. (Time needed for the delivery of the goods using this route). `Required` `Default(0)`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### DestinationStore

Obsolete. Not used. `Required` `Filter(multi eq)`

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### SourceStore

Obsolete. Not used. `Required` `Filter(multi eq)`

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### SupplySchema

The `SupplySchema`(Logistics.Inventory.SupplySchemaRoutes.md#supplyschema) to which this SupplySchemaRoute belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[SupplySchemata](Logistics.Inventory.SupplySchemata.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Inventory.SupplySchemaRoutes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.SupplySchemaRoutes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_SupplySchemaRoutes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_SupplySchemaRoutes?$top=10>

