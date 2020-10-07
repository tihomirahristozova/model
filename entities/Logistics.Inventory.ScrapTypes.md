# Logistics.Inventory.ScrapTypes

Types of scrap. Used in store transactions to categorize scrap, when it occurs. Entity: Inv_Scrap_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.ScrapTypes.md#Id) | guid |  
| [Description](Logistics.Inventory.ScrapTypes.md#Description) | string (nullable) | The description of this ScrapType. [Filter(like)] 
| [IsPlanned](Logistics.Inventory.ScrapTypes.md#IsPlanned) | boolean | True=Planned (expected) scrap. Scrap of this type will be used to refine planned scrap for future operations. 2=Unexpected scrap. [Required] [Default(true)] [Filter(eq)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Description

> The description of this ScrapType. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### IsPlanned

> True=Planned (expected) scrap. Scrap of this type will be used to refine planned scrap for future operations. 2=Unexpected scrap. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  



## Business Rules

[!list erp.entity=Logistics.Inventory.ScrapTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.ScrapTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.ScrapTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_ScrapTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_ScrapTypes?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Inv_Scrap_Types?$top=10>

