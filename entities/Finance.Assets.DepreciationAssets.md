---
uid: Finance.Assets.DepreciationAssets
---
# Finance.Assets.DepreciationAssets Entity

**Namespace:** [Finance.Assets](Finance.Assets.md)  

Depreciation document line. Can specify assets, whose depreciation should be calculated. Entity: Ast_Depreciation_Assets

## Default Visualization
Default Display Text Format:  
_{Depreciation.DocumentType.Code}:{Depreciation.DocumentNo} - {Depreciation.DocumentType.TypeName:T}_  
Default Search Member:  
_Depreciation.DocumentType.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Assets.Depreciations](Finance.Assets.Depreciations.md)  
Aggregate Root:  
[Finance.Assets.Depreciations](Finance.Assets.Depreciations.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Assets.DepreciationAssets.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Asset](Finance.Assets.DepreciationAssets.md#asset) | [Assets](Finance.Assets.Assets.md) | Specifies the asset, whose depreciation should be calculated with the current document. `Required` `Filter(multi eq)` |
| [Depreciation](Finance.Assets.DepreciationAssets.md#depreciation) | [Depreciations](Finance.Assets.Depreciations.md) | The `Depreciation`(Finance.Assets.DepreciationAssets.md#depreciation) to which this DepreciationAsset belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Asset

Specifies the asset, whose depreciation should be calculated with the current document. `Required` `Filter(multi eq)`

_Type_: **[Assets](Finance.Assets.Assets.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Depreciation

The `Depreciation`(Finance.Assets.DepreciationAssets.md#depreciation) to which this DepreciationAsset belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Depreciations](Finance.Assets.Depreciations.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Can filter by attributes of referenced entity_: **True**  



## Business Rules

[!list erp.entity=Finance.Assets.DepreciationAssets erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.DepreciationAssets erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_DepreciationAssets?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_DepreciationAssets?$top=10>

