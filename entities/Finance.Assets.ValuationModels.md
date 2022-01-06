---
uid: Finance.Assets.ValuationModels
---
# Finance.Assets.ValuationModels Entity

**Namespace:** [Finance.Assets](Finance.Assets.md)  

Valuation models stand for the different valuations an asset can have. For example Accounting, Tax, External Financial Reports, etc. All asset transactions are posted for specific valuation model, but are usually automatically copied to other models. Entity: Ast_Valuation_Models

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Assets.ValuationModels](Finance.Assets.ValuationModels.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Assets.ValuationModels.md#id) | guid |  
| [IsSystem](Finance.Assets.ValuationModels.md#issystem) | boolean | Is_System is True for those valuation models that are managed by the system via update procedures and cannot be edited by the user. `Required` `Default(false)` `Filter(eq)` `ReadOnly` 
| [Name](Finance.Assets.ValuationModels.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this ValuationModel. `Required` `Filter(like)` 
| [ObjectVersion](Finance.Assets.ValuationModels.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultDepreciationMethod](Finance.Assets.ValuationModels.md#defaultdepreciationmethod) | [DepreciationMethods](Finance.Assets.DepreciationMethods.md) (nullable) | Obsolete. Not used. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsSystem

Is_System is True for those valuation models that are managed by the system via update procedures and cannot be edited by the user. `Required` `Default(false)` `Filter(eq)` `ReadOnly`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

The name of this ValuationModel. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### DefaultDepreciationMethod

Obsolete. Not used. `Filter(multi eq)`

_Type_: **[DepreciationMethods](Finance.Assets.DepreciationMethods.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  


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



## Business Rules

[!list limit=1000 erp.entity=Finance.Assets.ValuationModels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Assets.ValuationModels erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_ValuationModels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_ValuationModels?$top=10>

