---
uid: Finance.Assets.AssetGroups
---
# Finance.Assets.AssetGroups Entity

**Namespace:** [Finance.Assets](Finance.Assets.md)  

User-defined grouping of the assets. Entity: Ast_Asset_Groups

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Assets.AssetGroups](Finance.Assets.AssetGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Assets.AssetGroups.md#code) | string (20) | The unique code of the AssetGroup. `Required` `Filter(eq)` `ORD` 
| [Id](Finance.Assets.AssetGroups.md#id) | guid |  
| [Name](Finance.Assets.AssetGroups.md#name) | string (254) | The name of this AssetGroup. `Required` `Filter(like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultValuationModel](Finance.Assets.AssetGroups.md#defaultvaluationmodel) | [ValuationModels](Finance.Assets.ValuationModels.md) (nullable) | Default valuation model when creating new assets from this group. `Filter(multi eq)` |
| [Parent](Finance.Assets.AssetGroups.md#parent) | [AssetGroups](Finance.Assets.AssetGroups.md) (nullable) | Parent asset group in the hierarchy. `Filter(multi eq)` |


## Attribute Details

### Code

The unique code of the AssetGroup. `Required` `Filter(eq)` `ORD`

_Type_: **string (20)**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Maximum Length_: **20**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this AssetGroup. `Required` `Filter(like)`

_Type_: **string (254)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### DefaultValuationModel

Default valuation model when creating new assets from this group. `Filter(multi eq)`

_Type_: **[ValuationModels](Finance.Assets.ValuationModels.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

Parent asset group in the hierarchy. `Filter(multi eq)`

_Type_: **[AssetGroups](Finance.Assets.AssetGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Assets.AssetGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.AssetGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_AssetGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_AssetGroups?$top=10>

