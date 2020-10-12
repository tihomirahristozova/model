---
uid: Finance.Assets.DepreciationPlanLineFixedValues
---
# Finance.Assets.DepreciationPlanLineFixedValues Entity

When specified, contains user-defined asset depreciation values for each depreciation period. Entity: Ast_Depreciation_Plan_Line_Fixed_Values

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DepreciationValue](Finance.Assets.DepreciationPlanLineFixedValues.md#depreciationvalue) | [Amount](../data-types.md#amount) | Fixed depreciation value for the period specified by Fixed_Value_Period_Month and Fixed_Value_Period_Year. [Currency: DepreciationPlanLine.Asset.ValuationCurrency] [Required] [Default(0)] 
| [FixedValuePeriodMonth](Finance.Assets.DepreciationPlanLineFixedValues.md#fixedvalueperiodmonth) | byte | Month of the period for which the depreciation value is fixed. [Required] 
| [FixedValuePeriodYear](Finance.Assets.DepreciationPlanLineFixedValues.md#fixedvalueperiodyear) | int16 | Year of the period for which the depreciation value is fixed. [Required] 
| [Id](Finance.Assets.DepreciationPlanLineFixedValues.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DepreciationPlanLine](Finance.Assets.DepreciationPlanLineFixedValues.md#depreciationplanline) | [DepreciationPlanLines](Finance.Assets.DepreciationPlanLines.md) | The [DepreciationPlanLine](Finance.Assets.DepreciationPlan<br />LineFixedValues.md#depreciationplanline) to which this DepreciationPlan<br />LineFixedValue belongs. [Required] [Filter(multi eq)]  |


## Attribute Details

### DepreciationValue

Fixed depreciation value for the period specified by Fixed_Value_Period_Month and Fixed_Value_Period_Year. [Currency: DepreciationPlanLine.Asset.ValuationCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### FixedValuePeriodMonth

Month of the period for which the depreciation value is fixed. [Required]

_Type_: **byte**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FixedValuePeriodYear

Year of the period for which the depreciation value is fixed. [Required]

_Type_: **int16**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### DepreciationPlanLine

The [DepreciationPlanLine](Finance.Assets.DepreciationPlanLineFixedValues.md#depreciationplanline) to which this DepreciationPlanLineFixedValue belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[DepreciationPlanLines](Finance.Assets.DepreciationPlanLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Assets.DepreciationPlanLineFixedValues erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.DepreciationPlanLineFixedValues erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_DepreciationPlanLineFixedValues?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_DepreciationPlanLineFixedValues?$top=10>

