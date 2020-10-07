# Finance.Assets.AssetCategories

Categorization of the assets, which specifies their depreciation plans. Entity: Ast_Asset_Categories

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Assets.AssetCategories.md#Id) | guid |  
| [Code](Finance.Assets.AssetCategories.md#Code) | string | The unique code of the AssetCategory. [Required] [Filter(eq)] [ORD] 
| [Name](Finance.Assets.AssetCategories.md#Name) | string | The name of this AssetCategory. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProductType](Finance.Assets.AssetCategories.md#ProductType) | [General.Products.ProductTypes](General.Products.ProductTypes.md) | Product type that correspondes to this category. Depreciation plan templates specified for this category will be used for the products of this type. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| DepreciationPlanTemplates | [Finance.Assets.DepreciationPlanTemplates](Finance.Assets.DepreciationPlanTemplates.md) | List of [DepreciationPlanTemplate](Finance.Assets.DepreciationPlanTemplates.md) child objects, based on the [Finance.Assets.DepreciationPlanTemplate.AssetCategory](Finance.Assets.DepreciationPlanTemplates.md#AssetCategory) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> The unique code of the AssetCategory. [Required] [Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### Name

> The name of this AssetCategory. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### ProductType

> Product type that correspondes to this category. Depreciation plan templates specified for this category will be used for the products of this type. [Required] [Filter(multi eq)]

_Type_: **[General.Products.ProductTypes](General.Products.ProductTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Assets.AssetCategories erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.AssetCategories erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Assets.AssetCategories erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_AssetCategories?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_AssetCategories?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Ast_Asset_Categories?$top=10>

