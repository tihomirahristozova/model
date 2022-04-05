---
uid: Finance.Excise.ExciseStampLots
---
# Finance.Excise.ExciseStampLots Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

Sequence of excise stamps with same production batch and type, received with one delivery. Entity: Exc_Excise_Stamp_Lots (Introduced in version 22.1.6.13)

## Default Visualization
Default Display Text Format:  
_{BatchNumber} {StartNumber}_  
Default Search Members:  
_BatchNumber_  
Code Data Member:  
_BatchNumber_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Excise.ExciseStampLots](Finance.Excise.ExciseStampLots.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BatchNumber](Finance.Excise.ExciseStampLots.md#batchnumber) | string (30) | Production batch of the Excise Stamps. `Required` `Filter(eq)` `ORD` 
| [DisplayText](Finance.Excise.ExciseStampLots.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [EndNumber](Finance.Excise.ExciseStampLots.md#endnumber) | string (30) | End number of the lot. `Required` 
| [Id](Finance.Excise.ExciseStampLots.md#id) | guid |  
| [IsActive](Finance.Excise.ExciseStampLots.md#isactive) | boolean | Is Active. `Required` `Default(true)` `Filter(eq)` 
| [ObjectVersion](Finance.Excise.ExciseStampLots.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [PurchaseLotNumber](Finance.Excise.ExciseStampLots.md#purchaselotnumber) | string (30) | Type and number of the document with which the excise stamps were received from the customs administration. `Required` 
| [Quantity](Finance.Excise.ExciseStampLots.md#quantity) | int32 | Number of excise stamps in the lot. `Required` `Default(0)` 
| [StartNumber](Finance.Excise.ExciseStampLots.md#startnumber) | string (30) | Start number of the lot. `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ExciseStampType](Finance.Excise.ExciseStampLots.md#excisestamptype) | [ExciseStampTypes](Finance.Excise.ExciseStampTypes.md) | Specifies the excise stamp type of the excise stamps in the lot. `Required` `Filter(multi eq)` |


## Attribute Details

### BatchNumber

Production batch of the Excise Stamps. `Required` `Filter(eq)` `ORD`

_Type_: **string (30)**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Maximum Length_: **30**  

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### EndNumber

End number of the lot. `Required`

_Type_: **string (30)**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **30**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Is Active. `Required` `Default(true)` `Filter(eq)`

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

### PurchaseLotNumber

Type and number of the document with which the excise stamps were received from the customs administration. `Required`

_Type_: **string (30)**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **30**  

### Quantity

Number of excise stamps in the lot. `Required` `Default(0)`

_Type_: **int32**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### StartNumber

Start number of the lot. `Required`

_Type_: **string (30)**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **30**  


## Reference Details

### ExciseStampType

Specifies the excise stamp type of the excise stamps in the lot. `Required` `Filter(multi eq)`

_Type_: **[ExciseStampTypes](Finance.Excise.ExciseStampTypes.md)**  
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



## Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExciseStampLots erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExciseStampLots erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Excise_ExciseStampLots?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Excise_ExciseStampLots?$top=10>
