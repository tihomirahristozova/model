---
uid: General.DocumentAmountTypes
---
# General.DocumentAmountTypes Entity

**Namespace:** [General](General.md)  

Represents the different types of additional amounts which are calculated for the documents. Entity: Gen_Document_Amount_Types

## Default Visualization
Default Display Text Format:  
_{AmountTypeCode}: {AmountTypeName:T}_  
Default Search Member:  
_AmountTypeCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.DocumentAmountTypes](General.DocumentAmountTypes.md)  
  * [General.DocumentAmountTypeDependencies](General.DocumentAmountTypeDependencies.md)  
  * [Finance.Intrastat.DocumentAmountTypeSettings](Finance.Intrastat.DocumentAmountTypeSettings.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AddToCustomer](General.DocumentAmountTypes.md#addtocustomer) | boolean | True means that the amount will be charged to the primary customer of the document. `Required` `Default(true)` 
| [AddToLine](General.DocumentAmountTypes.md#addtoline) | boolean | True means that the resulting amount will be added to the amount of each respective line. `Required` `Default(true)` 
| [AllowedDirections](General.DocumentAmountTypes.md#alloweddirections) | [AllowedDirections](General.DocumentAmountTypes.md#alloweddirections) (nullable) | Specifies condition for the sign of the allowed values for input percent or amount ​​that can be set in the documents. `Default(0)` 
| [AmountInputAllowed](General.DocumentAmountTypes.md#amountinputallowed) | boolean | True when the user is allowed to input fixed amount for distribution. `Required` `Default(false)` `Filter(eq)` 
| [AmountTypeCode](General.DocumentAmountTypes.md#amounttypecode) | string | A code that can be used to uniquely identify the additional amount. Can also be used for sorting purposes. `Required` `Filter(multi eq)` `ORD` 
| [AmountTypeName](General.DocumentAmountTypes.md#amounttypename) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of the amount type. `Required` `Filter(like)` `ORD` 
| [BaseOnLines](General.DocumentAmountTypes.md#baseonlines) | boolean | True means that the percentages will be applied over lines plus dependant amounts; false means only dependant amounts. `Required` `Default(true)` 
| [DefaultPercent](General.DocumentAmountTypes.md#defaultpercent) | decimal (nullable) | Default percent for amounts for which percent input is allowed; null otherwise. 
| [Description](General.DocumentAmountTypes.md#description) | string (nullable) | The description of this DocumentAmountType. 
| [DistributeBy](General.DocumentAmountTypes.md#distributeby) | [DistributeBy](General.DocumentAmountTypes.md#distributeby) | Specifies how the amount will be distributed among the document lines. Valid values are: ('AMOUNT','MEASUREMENT','PRODUCT DEFINITION'). `Required` `Default("AMOUNT")` `Filter(eq)` 
| [Id](General.DocumentAmountTypes.md#id) | guid |  
| [IsActive](General.DocumentAmountTypes.md#isactive) | boolean | True when the amount type is active for new records; false - otherwise. `Required` `Default(true)` `Filter(eq)` 
| [PercentInputAllowed](General.DocumentAmountTypes.md#percentinputallowed) | boolean | True when the user is allowed to input percent of total for distribution. `Required` `Default(true)` `Filter(eq)` 
| [RoundScale](General.DocumentAmountTypes.md#roundscale) | int32 (nullable) | The amounts should be rounded with the specified number of digits after the decimal point. null means to use the currency default. 
| [UnitAmountInputAllowed](General.DocumentAmountTypes.md#unitamountinputallowed) | boolean | Specifies whether the user is allowed to input fixed unit amount for the calculation of the amount. `Required` `Default(false)` `Filter(eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DistributeByMeasurement<br />Category](General.DocumentAmountTypes.md#distributebymeasurementcategory) | [MeasurementCategories](General.MeasurementCategories.md) (nullable) | Specifies the measurement category to be used for distribution, when the Distribute_By = 'MEASUREMENT'. `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Dependencies | [DocumentAmountTypeDependencies](General.DocumentAmountTypeDependencies.md) | List of `DocumentAmount<br />TypeDependency`(General.DocumentAmount<br />TypeDependencies.md) child objects, based on the `General.DocumentAmount<br />TypeDependency.DocumentAmountType`(General.DocumentAmount<br />TypeDependencies.md#documentamounttype) back reference 
| Settings | [DocumentAmountTypeSettings](Finance.Intrastat.DocumentAmountTypeSettings.md) | List of `DocumentAmount<br />TypeSetting`(Finance.Intrastat.DocumentAmountTypeSettings.md) child objects, based on the `Finance.Intrastat.DocumentAmountTypeSetting.DocumentAmountType`(Finance.Intrastat.DocumentAmountTypeSettings.md#documentamounttype) back reference 


## Attribute Details

### AddToCustomer

True means that the amount will be charged to the primary customer of the document. `Required` `Default(true)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### AddToLine

True means that the resulting amount will be added to the amount of each respective line. `Required` `Default(true)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### AllowedDirections

Specifies condition for the sign of the allowed values for input percent or amount ​​that can be set in the documents. `Default(0)`

_Type_: **[AllowedDirections](General.DocumentAmountTypes.md#alloweddirections) (nullable)**  
Allowed values for the `AllowedDirections`(General.DocumentAmountTypes.md#alloweddirections) data attribute  
_Allowed Values (General.DocumentAmountTypesRepository.AllowedDirections Enum Members)_  

| Value | Description |
| ---- | --- |
| AllowAll | AllowAll value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AllowAll' |
| AllowOnlyPositive | AllowOnlyPositive value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'AllowOnlyPositive' |
| AllowOnlyNegative | AllowOnlyNegative value. Stored as (-1). <br /> _Database Value:_ -1 <br /> _Model Value:_ -1 <br /> _Domain API Value:_ 'AllowOnlyNegative' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### AmountInputAllowed

True when the user is allowed to input fixed amount for distribution. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### AmountTypeCode

A code that can be used to uniquely identify the additional amount. Can also be used for sorting purposes. `Required` `Filter(multi eq)` `ORD`

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **True**  

### AmountTypeName

The name of the amount type. `Required` `Filter(like)` `ORD`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Indexed_: **True**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  

### BaseOnLines

True means that the percentages will be applied over lines plus dependant amounts; false means only dependant amounts. `Required` `Default(true)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### DefaultPercent

Default percent for amounts for which percent input is allowed; null otherwise.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( Not( obj.PercentInputAllowed), null, obj.DefaultPercent)`
### Description

The description of this DocumentAmountType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DistributeBy

Specifies how the amount will be distributed among the document lines. Valid values are: ('AMOUNT','MEASUREMENT','PRODUCT DEFINITION'). `Required` `Default("AMOUNT")` `Filter(eq)`

_Type_: **[DistributeBy](General.DocumentAmountTypes.md#distributeby)**  
Allowed values for the `DistributeBy`(General.DocumentAmountTypes.md#distributeby) data attribute  
_Allowed Values (General.DocumentAmountTypesRepository.DistributeBy Enum Members)_  

| Value | Description |
| ---- | --- |
| Amount | Amount value. Stored as 'AMOUNT'. <br /> _Database Value:_ 'AMOUNT' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Amount' |
| Measurement | Measurement value. Stored as 'MEASUREMENT'. <br /> _Database Value:_ 'MEASUREMENT' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Measurement' |
| ProductDefinition | ProductDefinition value. Stored as 'PRODUCT DEFINITION'. <br /> _Database Value:_ 'PRODUCT DEFINITION' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'ProductDefinition' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Amount**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

True when the amount type is active for new records; false - otherwise. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### PercentInputAllowed

True when the user is allowed to input percent of total for distribution. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### RoundScale

The amounts should be rounded with the specified number of digits after the decimal point. null means to use the currency default.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UnitAmountInputAllowed

Specifies whether the user is allowed to input fixed unit amount for the calculation of the amount. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### DistributeByMeasurementCategory

Specifies the measurement category to be used for distribution, when the Distribute_By = 'MEASUREMENT'. `Filter(multi eq)`

_Type_: **[MeasurementCategories](General.MeasurementCategories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( Convert( obj.DistributeBy, Int32) != 1), null, obj.DistributeByMeasurementCategory)`


## Business Rules

[!list erp.entity=General.DocumentAmountTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentAmountTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentAmountTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentAmountTypes?$top=10>

