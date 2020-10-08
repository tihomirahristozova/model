---
uid: Finance.Assets.DepreciationMethods
---
# Finance.Assets.DepreciationMethods

Depreciation methods. Contains both system-defined and user-defined methods. Entity: Ast_Depreciation_Methods

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Assets.DepreciationMethods.md#Id) | guid |  
| [DepreciationFunction](Finance.Assets.DepreciationMethods.md#DepreciationFunction) | [Finance.Assets.DepreciationMethodsRepository.DepreciationFunction](Finance.Assets.DepreciationMethods.md#DepreciationFunction) | Basic mathematical depreciation function used to calculate asset depreciation. STL=Straight Line, SYD=Sum of Years Digits, FAC=Depreciation change by factor, TAB=User defined with table. [Required] [Default("STL")] 
| [Name](Finance.Assets.DepreciationMethods.md#Name) | string | The name of this DepreciationMethod. [Required] [Filter(like)] 
| [Factor](Finance.Assets.DepreciationMethods.md#Factor) | decimal | Factor used in factor depreciation function. Factor < 1 means declining depreciation; >1 - increasing. The depreciation is multiplied for each period by the factor. [Required] [Default(1)] 
| [IsSystem](Finance.Assets.DepreciationMethods.md#IsSystem) | boolean | Is_System is True for those depreciation methods that are managed by the system via update procedures and cannot be edited by the user. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [MonthsInAPeriod](Finance.Assets.DepreciationMethods.md#MonthsInAPeriod) | int32 | Number of equal valued months calculated with single application of the function. [Required] [Default(12)] 
| [PeriodDeterminationMethod](Finance.Assets.DepreciationMethods.md#PeriodDeterminationMethod) | [Finance.Assets.DepreciationMethodsRepository.PeriodDeterminationMethod](Finance.Assets.DepreciationMethods.md#PeriodDeterminationMethod) | Determines when the depreciation starts and when it ends. NM=Next_Month, CM=Current_Month, BD=By_Days. [Required] 
| [StartFromNextMonth](Finance.Assets.DepreciationMethods.md#StartFromNextMonth) | boolean | When true, denotes that the depreciation starts from the month, following the month of deployment. When false, the depreciation starts from the same month. [Required] [Default(true)] [ReadOnly] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DepreciationFunction

> Basic mathematical depreciation function used to calculate asset depreciation. STL=Straight Line, SYD=Sum of Years Digits, FAC=Depreciation change by factor, TAB=User defined with table. [Required] [Default("STL")]

_Type_: **[Finance.Assets.DepreciationMethodsRepository.DepreciationFunction](Finance.Assets.DepreciationMethods.md#DepreciationFunction)**  
Allowed values for the [DepreciationFunction](Finance.Assets.DepreciationMethods.md#DepreciationFunction) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| DepreciationChangeByFactor | DepreciationChangeByFactor value. Stored as 'FAC'. <br /> _Database Value:_ 'FAC' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'DepreciationChangeByFactor' |
| StraightLine | StraightLine value. Stored as 'STL'. <br /> _Database Value:_ 'STL' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'StraightLine' |
| SumOfYearsDigits | SumOfYearsDigits value. Stored as 'SYD'. <br /> _Database Value:_ 'SYD' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'SumOfYearsDigits' |
| UserDefinedWithTable | UserDefinedWithTable value. Stored as 'TAB'. <br /> _Database Value:_ 'TAB' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'UserDefinedWithTable' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **StraightLine**  

### Name

> The name of this DepreciationMethod. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Factor

> Factor used in factor depreciation function. Factor < 1 means declining depreciation; >1 - increasing. The depreciation is multiplied for each period by the factor. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### IsSystem

> Is_System is True for those depreciation methods that are managed by the system via update procedures and cannot be edited by the user. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### MonthsInAPeriod

> Number of equal valued months calculated with single application of the function. [Required] [Default(12)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **12**  

### PeriodDeterminationMethod

> Determines when the depreciation starts and when it ends. NM=Next_Month, CM=Current_Month, BD=By_Days. [Required]

_Type_: **[Finance.Assets.DepreciationMethodsRepository.PeriodDeterminationMethod](Finance.Assets.DepreciationMethods.md#PeriodDeterminationMethod)**  
Allowed values for the [PeriodDeterminationMethod](Finance.Assets.DepreciationMethods.md#PeriodDeterminationMethod) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| NextMonth | NextMonth value. Stored as 'NM'. <br /> _Database Value:_ 'NM' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NextMonth' |
| CurrentMonth | CurrentMonth value. Stored as 'CM'. <br /> _Database Value:_ 'CM' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'CurrentMonth' |
| ByDays | ByDays value. Stored as 'BD'. <br /> _Database Value:_ 'BD' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'ByDays' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartFromNextMonth

> When true, denotes that the depreciation starts from the month, following the month of deployment. When false, the depreciation starts from the same month. [Required] [Default(true)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  



## Business Rules

[!list erp.entity=Finance.Assets.DepreciationMethods erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.DepreciationMethods erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Assets.DepreciationMethods erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_DepreciationMethods?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_DepreciationMethods?$top=10>

