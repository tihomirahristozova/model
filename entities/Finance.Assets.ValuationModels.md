---
uid: Finance.Assets.ValuationModels
---
# Finance.Assets.ValuationModels Entity

Valuation models stand for the different valuations an asset can have. For example Accounting, Tax, External Financial Reports, etc. All asset transactions are posted for specific valuation model, but are usually automatically copied to other models. Entity: Ast_Valuation_Models

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Assets.ValuationModels.md#id) | guid |  
| [IsSystem](Finance.Assets.ValuationModels.md#issystem) | boolean | Is_System is True for those valuation models that are managed by the system via update procedures and cannot be edited by the user. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [Name](Finance.Assets.ValuationModels.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this ValuationModel. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultDepreciationMethod](Finance.Assets.ValuationModels.md#defaultdepreciationmethod) | [DepreciationMethods](Finance.Assets.DepreciationMethods.md) (nullable) | Obsolete. Not used. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsSystem

Is_System is True for those valuation models that are managed by the system via update procedures and cannot be edited by the user. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

The name of this ValuationModel. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### DefaultDepreciationMethod

Obsolete. Not used. [Filter(multi eq)]

_Type_: **[DepreciationMethods](Finance.Assets.DepreciationMethods.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Assets.ValuationModels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.ValuationModels erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_ValuationModels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_ValuationModels?$top=10>

