# General.DocumentAmountTypeDependencies

Specifies the base amounts on which an amount depends. . Entity: Gen_Document_Amount_Type_Dependencies

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentAmountTypeDependencies.md#Id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DependsOnDocumentAmountType](General.DocumentAmountTypeDependencies.md#DependsOnDocumentAmountType) | [General.DocumentAmountTypes](General.DocumentAmountTypes.md) | The base amount type on which the current amount depends. [Required] [Filter(multi eq)] |
| [DocumentAmountType](General.DocumentAmountTypeDependencies.md#DocumentAmountType) | [General.DocumentAmountTypes](General.DocumentAmountTypes.md) | The amount for which the base amount is specified. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  


## Reference Details

### DependsOnDocumentAmountType

> The base amount type on which the current amount depends. [Required] [Filter(multi eq)]

_Type_: **[General.DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DocumentAmountType

> The amount for which the base amount is specified. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.DocumentAmountTypeDependencies erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentAmountTypeDependencies erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentAmountTypeDependencies erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentAmountTypeDependencies?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentAmountTypeDependencies?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Document_Amount_Type_Dependencies?$top=10>

