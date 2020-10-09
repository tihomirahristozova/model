---
uid: Finance.Assets.DepreciationPlanLines
---
# Finance.Assets.DepreciationPlanLines Entity

Each record contains one depreciation plan for one valuation model of one asset. Entity: Ast_Depreciation_Plan_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DepreciationEndDate](Finance.Assets.DepreciationPlanLines.md#depreciationenddate) | datetime | End date of the depreciation plan for this asset. [Required] 
| [DepreciationStartDate](Finance.Assets.DepreciationPlanLines.md#depreciationstartdate) | datetime | Start date of the depreciation plan for this asset. [Required] 
| [Id](Finance.Assets.DepreciationPlanLines.md#id) | guid |  
| [LineNo](Finance.Assets.DepreciationPlanLines.md#lineno) | int32 | Consecutive number of the line within the depreciation plan. [Required] [Filter(eq)] 
| [PlanDepreciationValue](Finance.Assets.DepreciationPlanLines.md#plandepreciationvalue) | [Amount](../data-types.md#amount) | The part of the total amount of the asset (in the currency of the asset), which is due for depreciation. [Currency: Asset.ValuationCurrency] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Asset](Finance.Assets.DepreciationPlanLines.md#asset) | [Assets](Finance.Assets.Assets.md) | The asset that is planned for depreciation. [Required] [Filter(multi eq)] |
| [DepreciationMethod](Finance.Assets.DepreciationPlanLines.md#depreciationmethod) | [DepreciationMethods](Finance.Assets.DepreciationMethods.md) | Depreciation method by which the asset will be depreciated. [Required] [Filter(multi eq)] |
| [DepreciationPlan](Finance.Assets.DepreciationPlanLines.md#depreciationplan) | [DepreciationPlans](Finance.Assets.DepreciationPlans.md) | The [DepreciationPlan](Finance.Assets.DepreciationPlanLines.md#depreciationplan) to which this DepreciationPlanLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [ValuationModel](Finance.Assets.DepreciationPlanLines.md#valuationmodel) | [ValuationModels](Finance.Assets.ValuationModels.md) | Valuation model in which the asset is accounted. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| FixedValues | [DepreciationPlanLineFixedValues](Finance.Assets.DepreciationPlanLineFixedValues.md) | List of [DepreciationPlan<br />LineFixedValue](Finance.Assets.DepreciationPlan<br />LineFixedValues.md) child objects, based on the [Finance.Assets.DepreciationPlan<br />LineFixedValue.DepreciationPlanLine](Finance.Assets.DepreciationPlan<br />LineFixedValues.md#depreciationplanline) back  


## Attribute Details

### DepreciationEndDate

> End date of the depreciation plan for this asset. [Required]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DepreciationStartDate

> Start date of the depreciation plan for this asset. [Required]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

> Consecutive number of the line within the depreciation plan. [Required] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.DepreciationPlan.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.DepreciationPlan.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### PlanDepreciationValue

> The part of the total amount of the asset (in the currency of the asset), which is due for depreciation. [Currency: Asset.ValuationCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### Asset

> The asset that is planned for depreciation. [Required] [Filter(multi eq)]

_Type_: **[Assets](Finance.Assets.Assets.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### DepreciationMethod

> Depreciation method by which the asset will be depreciated. [Required] [Filter(multi eq)]

_Type_: **[DepreciationMethods](Finance.Assets.DepreciationMethods.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### DepreciationPlan

> The [DepreciationPlan](Finance.Assets.DepreciationPlanLines.md#depreciationplan) to which this DepreciationPlanLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[DepreciationPlans](Finance.Assets.DepreciationPlans.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ValuationModel

> Valuation model in which the asset is accounted. [Required] [Filter(multi eq)]

_Type_: **[ValuationModels](Finance.Assets.ValuationModels.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Assets.DepreciationPlanLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.DepreciationPlanLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Assets.DepreciationPlanLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_DepreciationPlanLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_DepreciationPlanLines?$top=10>

