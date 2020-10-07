# General.DocumentAmountTypes

Represents the different types of additional amounts which are calculated for the documents. Entity: Gen_Document_Amount_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentAmountTypes.md#Id) | guid |  
| [AddToCustomer](General.DocumentAmountTypes.md#AddToCustomer) | boolean | True means that the amount will be charged to the primary customer of the document. [Required] [Default(true)] 
| [AddToLine](General.DocumentAmountTypes.md#AddToLine) | boolean | True means that the resulting amount will be added to the amount of each respective line. [Required] [Default(true)] 
| [AllowedDirections](General.DocumentAmountTypes.md#AllowedDirections) | [General.DocumentAmountTypesRepository.AllowedDirections](General.DocumentAmountTypes.md#AllowedDirections) (nullable) | Specifies condition for the sign of the allowed values for input percent or amount ​​that can be set in the documents. [Default(0)] 
| [AmountInputAllowed](General.DocumentAmountTypes.md#AmountInputAllowed) | boolean | True when the user is allowed to input fixed amount for distribution. [Required] [Default(false)] [Filter(eq)] 
| [AmountTypeCode](General.DocumentAmountTypes.md#AmountTypeCode) | string | A code that can be used to uniquely identify the additional amount. Can also be used for sorting purposes. [Required] [Filter(multi eq)] [ORD] 
| [AmountTypeName](General.DocumentAmountTypes.md#AmountTypeName) | [MultilanguageString](../data-types/MultilanguageString.md) | The name of the amount type. [Required] [Filter(like)] [ORD] 
| [BaseOnLines](General.DocumentAmountTypes.md#BaseOnLines) | boolean | True means that the percentages will be applied over lines plus dependant amounts; false means only dependant amounts. [Required] [Default(true)] 
| [DefaultPercent](General.DocumentAmountTypes.md#DefaultPercent) | decimal (nullable) | Default percent for amounts for which percent input is allowed; null otherwise. 
| [Description](General.DocumentAmountTypes.md#Description) | string (nullable) | The description of this DocumentAmountType. 
| [DistributeBy](General.DocumentAmountTypes.md#DistributeBy) | [General.DocumentAmountTypesRepository.DistributeBy](General.DocumentAmountTypes.md#DistributeBy) | Specifies how the amount will be distributed among the document lines. Valid values are: ('AMOUNT','MEASUREMENT','PRODUCT DEFINITION'). [Required] [Default("AMOUNT")] [Filter(eq)] 
| [IsActive](General.DocumentAmountTypes.md#IsActive) | boolean | True when the amount type is active for new records; false - otherwise. [Required] [Default(true)] [Filter(eq)] 
| [PercentInputAllowed](General.DocumentAmountTypes.md#PercentInputAllowed) | boolean | True when the user is allowed to input percent of total for distribution. [Required] [Default(true)] [Filter(eq)] 
| [RoundScale](General.DocumentAmountTypes.md#RoundScale) | int32 (nullable) | The amounts should be rounded with the specified number of digits after the decimal point. null means to use the currency default. 
| [UnitAmountInputAllowed](General.DocumentAmountTypes.md#UnitAmountInputAllowed) | boolean | Specifies whether the user is allowed to input fixed unit amount for the calculation of the amount. [Required] [Default(false)] [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DistributeByMeasurementCategory](General.DocumentAmountTypes.md#DistributeByMeasurementCategory) | [General.MeasurementCategories](General.MeasurementCategories.md) (nullable) | Specifies the measurement category to be used for distribution, when the Distribute_By = 'MEASUREMENT'. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Dependencies | [General.DocumentAmountTypeDependencies](General.DocumentAmountTypeDependencies.md) | List of [DocumentAmountTypeDependency](General.DocumentAmountTypeDependencies.md) child objects, based on the [General.DocumentAmountTypeDependency.DocumentAmountType](General.DocumentAmountTypeDependencies.md#DocumentAmountType) back reference 
| Settings | [Finance.Intrastat.DocumentAmountTypeSettings](Finance.Intrastat.DocumentAmountTypeSettings.md) | List of [DocumentAmountTypeSetting](Finance.Intrastat.DocumentAmountTypeSettings.md) child objects, based on the [Finance.Intrastat.DocumentAmountTypeSetting.DocumentAmountType](Finance.Intrastat.DocumentAmountTypeSettings.md#DocumentAmountType) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AddToCustomer

> True means that the amount will be charged to the primary customer of the document. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### AddToLine

> True means that the resulting amount will be added to the amount of each respective line. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### AllowedDirections

> Specifies condition for the sign of the allowed values for input percent or amount ​​that can be set in the documents. [Default(0)]

_Type_: **[General.DocumentAmountTypesRepository.AllowedDirections](General.DocumentAmountTypes.md#AllowedDirections) (nullable)**  
Allowed values for the [AllowedDirections](General.DocumentAmountTypes.md#AllowedDirections) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| AllowAll | AllowAll value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AllowAll' |
| AllowOnlyPositive | AllowOnlyPositive value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'AllowOnlyPositive' |
| AllowOnlyNegative | AllowOnlyNegative value. Stored as (-1). <br /> _Database Value:_ -1 <br /> _Model Value:_ -1 <br /> _Domain API Value:_ 'AllowOnlyNegative' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### AmountInputAllowed

> True when the user is allowed to input fixed amount for distribution. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### AmountTypeCode

> A code that can be used to uniquely identify the additional amount. Can also be used for sorting purposes. [Required] [Filter(multi eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **True**  

### AmountTypeName

> The name of the amount type. [Required] [Filter(like)] [ORD]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  

### BaseOnLines

> True means that the percentages will be applied over lines plus dependant amounts; false means only dependant amounts. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### DefaultPercent

> Default percent for amounts for which percent input is allowed; null otherwise.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Description

> The description of this DocumentAmountType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DistributeBy

> Specifies how the amount will be distributed among the document lines. Valid values are: ('AMOUNT','MEASUREMENT','PRODUCT DEFINITION'). [Required] [Default("AMOUNT")] [Filter(eq)]

_Type_: **[General.DocumentAmountTypesRepository.DistributeBy](General.DocumentAmountTypes.md#DistributeBy)**  
Allowed values for the [DistributeBy](General.DocumentAmountTypes.md#DistributeBy) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Amount | Amount value. Stored as 'AMOUNT'. <br /> _Database Value:_ 'AMOUNT' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Amount' |
| Measurement | Measurement value. Stored as 'MEASUREMENT'. <br /> _Database Value:_ 'MEASUREMENT' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Measurement' |
| ProductDefinition | ProductDefinition value. Stored as 'PRODUCT DEFINITION'. <br /> _Database Value:_ 'PRODUCT DEFINITION' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'ProductDefinition' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Amount**  

### IsActive

> True when the amount type is active for new records; false - otherwise. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### PercentInputAllowed

> True when the user is allowed to input percent of total for distribution. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### RoundScale

> The amounts should be rounded with the specified number of digits after the decimal point. null means to use the currency default.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UnitAmountInputAllowed

> Specifies whether the user is allowed to input fixed unit amount for the calculation of the amount. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### DistributeByMeasurementCategory

> Specifies the measurement category to be used for distribution, when the Distribute_By = 'MEASUREMENT'. [Filter(multi eq)]

_Type_: **[General.MeasurementCategories](General.MeasurementCategories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.DocumentAmountTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentAmountTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentAmountTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentAmountTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentAmountTypes?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Document_Amount_Types?$top=10>

