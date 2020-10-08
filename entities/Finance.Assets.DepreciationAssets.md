---
uid: Finance.Assets.DepreciationAssets
---
# Finance.Assets.DepreciationAssets

Depreciation document line. Can specify assets, whose depreciation should be calculated. Entity: Ast_Depreciation_Assets

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Assets.DepreciationAssets.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Asset](Finance.Assets.DepreciationAssets.md#asset) | [Finance.Assets.Assets](Finance.Assets.Assets.md) | Specifies the asset, whose depreciation should be calculated with the current document. [Required] [Filter(multi eq)] |
| [Depreciation](Finance.Assets.DepreciationAssets.md#depreciation) | [Finance.Assets.Depreciations](Finance.Assets.Depreciations.md) | The [Depreciation](Finance.Assets.DepreciationAssets.md#depreciation) to which this DepreciationAsset belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Asset

> Specifies the asset, whose depreciation should be calculated with the current document. [Required] [Filter(multi eq)]

_Type_: **[Finance.Assets.Assets](Finance.Assets.Assets.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Depreciation

> The [Depreciation](Finance.Assets.DepreciationAssets.md#depreciation) to which this DepreciationAsset belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Assets.Depreciations](Finance.Assets.Depreciations.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Assets.DepreciationAssets erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.DepreciationAssets erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Assets.DepreciationAssets erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_DepreciationAssets?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_DepreciationAssets?$top=10>

