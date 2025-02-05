---
uid: General.DocumentAmountTypes
---
# General.DocumentAmountTypes Entity

**Namespace:** [General](General.md)  

Represents the different types of additional amounts which are calculated for the documents. Entity: Gen_Document_Amount_Types

## Default Visualization
Default Display Text Format:  
_{AmountTypeName:T}_  
Default Search Members:  
_AmountTypeCode; AmountTypeName_  
Code Data Member:  
_AmountTypeCode_  
Name Data Member:  
_AmountTypeName_  

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
| [AllowedDirections](General.DocumentAmountTypes.md#alloweddirections) | [AllowedDirections](General.DocumentAmountTypes.md#alloweddirections) __nullable__ | Specifies condition for the sign of the allowed values for input percent or amount ​​that can be set in the documents. `Default(0)` 
| [AmountInputAllowed](General.DocumentAmountTypes.md#amountinputallowed) | boolean | True when the user is allowed to input fixed amount for distribution. `Required` `Default(false)` `Filter(eq)` 
| [AmountTypeCode](General.DocumentAmountTypes.md#amounttypecode) | string (16) | A code that can be used to uniquely identify the additional amount. Can also be used for sorting purposes. `Required` `Filter(multi eq)` `ORD` 
| [AmountTypeName](General.DocumentAmountTypes.md#amounttypename) | [MultilanguageString (128)](../data-types.md#multilanguagestring) | The name of the amount type. `Required` `Filter(like)` `ORD` 
| [BaseOnLines](General.DocumentAmountTypes.md#baseonlines) | boolean | True means that the percentages will be applied over lines plus dependant amounts; false means only dependant amounts. `Required` `Default(true)` 
| [DefaultPercent](General.DocumentAmountTypes.md#defaultpercent) | decimal (7, 6) __nullable__ | Default percent for amounts for which percent input is allowed; null otherwise. 
| [Description](General.DocumentAmountTypes.md#description) | string (254) __nullable__ | The description of this DocumentAmountType. 
| [DisplayText](General.DocumentAmountTypes.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [DistributeBy](General.DocumentAmountTypes.md#distributeby) | [DistributeBy](General.DocumentAmountTypes.md#distributeby) | Specifies how the amount will be distributed among the document lines. Valid values are: ('AMOUNT','MEASUREMENT','PRODUCT DEFINITION','DEAL TYPE'). `Required` `Default("AMOUNT")` `Filter(eq)` 
| [Id](General.DocumentAmountTypes.md#id) | guid |  
| [IsActive](General.DocumentAmountTypes.md#isactive) | boolean | True when the amount type is active for new records; false - otherwise. `Required` `Default(true)` `Filter(eq)` 
| [ObjectVersion](General.DocumentAmountTypes.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [PercentInputAllowed](General.DocumentAmountTypes.md#percentinputallowed) | boolean | True when the user is allowed to input percent of total for distribution. `Required` `Default(true)` `Filter(eq)` 
| [RoundScale](General.DocumentAmountTypes.md#roundscale) | int32 __nullable__ | The amounts should be rounded with the specified number of digits after the decimal point. null means to use the currency default. 
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
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### AddToLine

True means that the resulting amount will be added to the amount of each respective line. `Required` `Default(true)`

_Type_: **boolean**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### AllowedDirections

Specifies condition for the sign of the allowed values for input percent or amount ​​that can be set in the documents. `Default(0)`

_Type_: **[AllowedDirections](General.DocumentAmountTypes.md#alloweddirections) __nullable__**  
_Category_: **System**  
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
_Category_: **System**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### AmountTypeCode

A code that can be used to uniquely identify the additional amount. Can also be used for sorting purposes. `Required` `Filter(multi eq)` `ORD`

_Type_: **string (16)**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **True**  
_Maximum Length_: **16**  

### AmountTypeName

The name of the amount type. `Required` `Filter(like)` `ORD`

_Type_: **[MultilanguageString (128)](../data-types.md#multilanguagestring)**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  

### BaseOnLines

True means that the percentages will be applied over lines plus dependant amounts; false means only dependant amounts. `Required` `Default(true)`

_Type_: **boolean**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### DefaultPercent

Default percent for amounts for which percent input is allowed; null otherwise.

_Type_: **decimal (7, 6) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( Not( obj.PercentInputAllowed), null, obj.DefaultPercent)`
### Description

The description of this DocumentAmountType.

_Type_: **string (254) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### DistributeBy

Specifies how the amount will be distributed among the document lines. Valid values are: ('AMOUNT','MEASUREMENT','PRODUCT DEFINITION','DEAL TYPE'). `Required` `Default("AMOUNT")` `Filter(eq)`

_Type_: **[DistributeBy](General.DocumentAmountTypes.md#distributeby)**  
_Category_: **System**  
Allowed values for the `DistributeBy`(General.DocumentAmountTypes.md#distributeby) data attribute  
_Allowed Values (General.DocumentAmountTypesRepository.DistributeBy Enum Members)_  

| Value | Description |
| ---- | --- |
| Amount | Amount value. Stored as 'AMOUNT'. <br /> _Database Value:_ 'AMOUNT' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Amount' |
| Measurement | Measurement value. Stored as 'MEASUREMENT'. <br /> _Database Value:_ 'MEASUREMENT' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Measurement' |
| ProductDefinition | ProductDefinition value. Stored as 'PRODUCT DEFINITION'. <br /> _Database Value:_ 'PRODUCT DEFINITION' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'ProductDefinition' |
| DealType | DealType value. Stored as 'DEAL TYPE'. <br /> _Database Value:_ 'DEAL TYPE' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'DealType' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Amount**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

True when the amount type is active for new records; false - otherwise. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Category_: **System**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### PercentInputAllowed

True when the user is allowed to input percent of total for distribution. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Category_: **System**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### RoundScale

The amounts should be rounded with the specified number of digits after the decimal point. null means to use the currency default.

_Type_: **int32 __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UnitAmountInputAllowed

Specifies whether the user is allowed to input fixed unit amount for the calculation of the amount. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Category_: **System**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### DistributeByMeasurementCategory

Specifies the measurement category to be used for distribution, when the Distribute_By = 'MEASUREMENT'. `Filter(multi eq)`

_Type_: **[MeasurementCategories](General.MeasurementCategories.md) (nullable)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( Convert( obj.DistributeBy, Int32) != 1), null, obj.DistributeByMeasurementCategory)`

## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  


### CreateNotification

Creates a notification a sends a real time event to the user.  
_Return Type_: **void**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  

**Parameters**  
  * **user**  
    The user.  
    _Type_: [Users](Systems.Security.Users.md)  

  * **notificationClass**  
    The notification class.  
    _Type_: string  

  * **subject**  
    The subject.  
    _Type_: string  


### CreateCopy

Duplicates the object and its child objects belonging to the same aggregate.              The duplicated objects are not saved to the data source but remain in the same transaction as the original object.  
_Return Type_: **EntityObject**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  


## Business Rules

[!list limit=1000 erp.entity=General.DocumentAmountTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentAmountTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentAmountTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentAmountTypes?$top=10>

