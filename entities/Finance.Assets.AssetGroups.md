---
uid: Finance.Assets.AssetGroups
---
# Finance.Assets.AssetGroups

User-defined grouping of the assets. Entity: Ast_Asset_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Assets.AssetGroups.md#Id) | guid |  
| [Code](Finance.Assets.AssetGroups.md#Code) | string | The unique code of the AssetGroup. [Required] [Filter(eq)] [ORD] 
| [Name](Finance.Assets.AssetGroups.md#Name) | string | The name of this AssetGroup. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultValuationModel](Finance.Assets.AssetGroups.md#DefaultValuationModel) | [Finance.Assets.ValuationModels](Finance.Assets.ValuationModels.md) (nullable) | Default valuation model when creating new assets from this group. [Filter(multi eq)] |
| [Parent](Finance.Assets.AssetGroups.md#Parent) | [Finance.Assets.AssetGroups](Finance.Assets.AssetGroups.md) (nullable) | Parent asset group in the hierarchy. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> The unique code of the AssetGroup. [Required] [Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### Name

> The name of this AssetGroup. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### DefaultValuationModel

> Default valuation model when creating new assets from this group. [Filter(multi eq)]

_Type_: **[Finance.Assets.ValuationModels](Finance.Assets.ValuationModels.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Parent

> Parent asset group in the hierarchy. [Filter(multi eq)]

_Type_: **[Finance.Assets.AssetGroups](Finance.Assets.AssetGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Assets.AssetGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.AssetGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Assets.AssetGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_AssetGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_AssetGroups?$top=10>

