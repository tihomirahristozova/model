---
uid: Finance.Accounting.ProfitCenters
---
# Finance.Accounting.ProfitCenters Entity

**Namespace:** [Finance.Accounting](Finance.Accounting.md)  

Defines company profit centers and their relative weight for automatic balance transfers from cost centers. Entity: Acc_Profit_Centers

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  
Name Data Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Accounting.ProfitCenters](Finance.Accounting.ProfitCenters.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](Finance.Accounting.ProfitCenters.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [Id](Finance.Accounting.ProfitCenters.md#id) | guid |  
| [Name](Finance.Accounting.ProfitCenters.md#name) | string (254) | The name of this ProfitCenter. `Required` `Filter(like)` 
| [Notes](Finance.Accounting.ProfitCenters.md#notes) | string (254) __nullable__ | Notes for this ProfitCenter. 
| [ObjectVersion](Finance.Accounting.ProfitCenters.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [RelativeWeight](Finance.Accounting.ProfitCenters.md#relativeweight) | decimal (18, 4) | The weight of this profit center, relative to the other profit centers within the same parent. The weight is used during profit distribution calculations. The sum of weights of all profit centers within a parent does not need to be 100, the ratio of total weight over weight is used. `Required` `Default(1)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Finance.Accounting.ProfitCenters.md#parent) | [ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable) | Parent profit center, null if this is root profit center. `Filter(multi eq)` |


## Attribute Details

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this ProfitCenter. `Required` `Filter(like)`

_Type_: **string (254)**  
_Category_: **System**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Notes

Notes for this ProfitCenter.

_Type_: **string (254) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### RelativeWeight

The weight of this profit center, relative to the other profit centers within the same parent. The weight is used during profit distribution calculations. The sum of weights of all profit centers within a parent does not need to be 100, the ratio of total weight over weight is used. `Required` `Default(1)`

_Type_: **decimal (18, 4)**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### Parent

Parent profit center, null if this is root profit center. `Filter(multi eq)`

_Type_: **[ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable)**  
_Category_: **System**  
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

[!list limit=1000 erp.entity=Finance.Accounting.ProfitCenters erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.ProfitCenters erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_ProfitCenters?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_ProfitCenters?$top=10>

