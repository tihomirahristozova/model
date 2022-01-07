---
uid: Finance.Cost.AllocationModels
---
# Finance.Cost.AllocationModels Entity

**Namespace:** [Finance.Cost](Finance.Cost.md)  

User-defined models for cost allocation. Entity: Cost_Allocation_Models

## Default Visualization
Default Display Text Format:  
_{CostAllocationModelName}_  
Default Search Members:  
_CostAllocationModelName_  
Name Data Member:  
_CostAllocationModelName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Cost.AllocationModels](Finance.Cost.AllocationModels.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CostAllocationModelName](Finance.Cost.AllocationModels.md#costallocationmodelname) | string (254) | Multilanguage allocation model name. `Required` 
| [DisplayText](Finance.Cost.AllocationModels.md#displaytext) | string |  
| [Id](Finance.Cost.AllocationModels.md#id) | guid |  
| [ObjectVersion](Finance.Cost.AllocationModels.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Currency](Finance.Cost.AllocationModels.md#currency) | [Currencies](General.Currencies.md) | The currency in which the calculation is done. This is applied to the production and the results. `Required` `Filter(multi eq)` |


## Attribute Details

### CostAllocationModelName

Multilanguage allocation model name. `Required`

_Type_: **string (254)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### DisplayText

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### Currency

The currency in which the calculation is done. This is applied to the production and the results. `Required` `Filter(multi eq)`

_Type_: **[Currencies](General.Currencies.md)**  
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

[!list limit=1000 erp.entity=Finance.Cost.AllocationModels erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Cost.AllocationModels erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_AllocationModels?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_AllocationModels?$top=10>

