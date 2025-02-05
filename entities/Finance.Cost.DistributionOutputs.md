---
uid: Finance.Cost.DistributionOutputs
---
# Finance.Cost.DistributionOutputs Entity

**Namespace:** [Finance.Cost](Finance.Cost.md)  

Contains the output data for the specified period. This is the output on which cost is distributed. Entity: Cost_Distribution_Outputs

## Default Visualization
Default Display Text Format:  
_{CostDistribution.EntityName}_  
Default Search Members:  
_CostDistribution.EntityName_  
Name Data Member:  
_CostDistribution.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Cost.Distributions](Finance.Cost.Distributions.md)  
Aggregate Root:  
[Finance.Cost.Distributions](Finance.Cost.Distributions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](Finance.Cost.DistributionOutputs.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [Id](Finance.Cost.DistributionOutputs.md#id) | guid |  
| [LineNo](Finance.Cost.DistributionOutputs.md#lineno) | int32 | Unique (within the document), consecutive line number of the output. `Required` 
| [ObjectVersion](Finance.Cost.DistributionOutputs.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [WeightCoefficient](Finance.Cost.DistributionOutputs.md#weightcoefficient) | decimal (12, 5) | The weight coefficient for prorate distribution of cost over the current line. `Required` `Default(1)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CostDistribution](Finance.Cost.DistributionOutputs.md#costdistribution) | [Distributions](Finance.Cost.Distributions.md) | The <see cref="Distribution"/> to which this DistributionOutput belongs. `Required` `Filter(multi eq)` `Owner` |
| [StoreTransactionLine](Finance.Cost.DistributionOutputs.md#storetransactionline) | [StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md) | The store transaction line, for which costs will be distributed. `Required` `Filter(multi eq)` |


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

### LineNo

Unique (within the document), consecutive line number of the output. `Required`

_Type_: **int32**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.CostDistribution.Outputs.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.CostDistribution.Outputs.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### WeightCoefficient

The weight coefficient for prorate distribution of cost over the current line. `Required` `Default(1)`

_Type_: **decimal (12, 5)**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### CostDistribution

The <see cref="Distribution"/> to which this DistributionOutput belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Distributions](Finance.Cost.Distributions.md)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### StoreTransactionLine

The store transaction line, for which costs will be distributed. `Required` `Filter(multi eq)`

_Type_: **[StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md)**  
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

[!list limit=1000 erp.entity=Finance.Cost.DistributionOutputs erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Cost.DistributionOutputs erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_DistributionOutputs?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_DistributionOutputs?$top=10>

