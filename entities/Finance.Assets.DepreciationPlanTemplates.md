---
uid: Finance.Assets.DepreciationPlanTemplates
---
# Finance.Assets.DepreciationPlanTemplates Entity

**Namespace:** [Finance.Assets](Finance.Assets.md)  

Specifies the default depreciation methods for the asset categories. Different methods can be specified for each valuation model. Entity: Ast_Depreciation_Plan_Templates

## Default Visualization
Default Display Text Format:  
_{AssetCategory.Code}: {AssetCategory.Name:T}_  
Default Search Member:  
_AssetCategory.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Assets.AssetCategories](Finance.Assets.AssetCategories.md)  
Aggregate Root:  
[Finance.Assets.AssetCategories](Finance.Assets.AssetCategories.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AssetLife](Finance.Assets.DepreciationPlanTemplates.md#assetlife) | int32 __nullable__ | Asset life in months by default for the depreciation plans created by this template. null means that the asset is booked for this valuation model but is not depreciated in it (i.e. no depreciation plan is created). 
| [Id](Finance.Assets.DepreciationPlanTemplates.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AssetCategory](Finance.Assets.DepreciationPlanTemplates.md#assetcategory) | [AssetCategories](Finance.Assets.AssetCategories.md) | Asset category for which this template is defined. `Required` `Filter(multi eq)` `Owner` |
| [DepreciationMethod](Finance.Assets.DepreciationPlanTemplates.md#depreciationmethod) | [DepreciationMethods](Finance.Assets.DepreciationMethods.md) | Depreciation method by default for the depreciation plans created by this template. `Required` `Filter(multi eq)` |
| [ValuationModel](Finance.Assets.DepreciationPlanTemplates.md#valuationmodel) | [ValuationModels](Finance.Assets.ValuationModels.md) | Valuation model for which this template is defined. `Required` `Filter(multi eq)` |


## Attribute Details

### AssetLife

Asset life in months by default for the depreciation plans created by this template. null means that the asset is booked for this valuation model but is not depreciated in it (i.e. no depreciation plan is created).

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### AssetCategory

Asset category for which this template is defined. `Required` `Filter(multi eq)` `Owner`

_Type_: **[AssetCategories](Finance.Assets.AssetCategories.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### DepreciationMethod

Depreciation method by default for the depreciation plans created by this template. `Required` `Filter(multi eq)`

_Type_: **[DepreciationMethods](Finance.Assets.DepreciationMethods.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ValuationModel

Valuation model for which this template is defined. `Required` `Filter(multi eq)`

_Type_: **[ValuationModels](Finance.Assets.ValuationModels.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Assets.DepreciationPlanTemplates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.DepreciationPlanTemplates erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_DepreciationPlanTemplates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_DepreciationPlanTemplates?$top=10>

