---
uid: Logistics.Inventory.SupplySchemata
---
# Logistics.Inventory.SupplySchemata

Obsolete. Not used. Entity: Inv_Supply_Schemata

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.SupplySchemata.md#id) | guid |  
| [Name](Logistics.Inventory.SupplySchemata.md#name) | string | The name of this SupplySchema. [Required] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Routes | [Logistics.Inventory.SupplySchemaRoutes](Logistics.Inventory.SupplySchemaRoutes.md) | List of [SupplySchemaRoute](Logistics.Inventory.SupplySchemaRoutes.md) child objects, based on the [Logistics.Inventory.SupplySchemaRoute.SupplySchema](Logistics.Inventory.SupplySchemaRoutes.md#supplyschema) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> The name of this SupplySchema. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.SupplySchemata erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.SupplySchemata erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.SupplySchemata erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_SupplySchemata?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_SupplySchemata?$top=10>

