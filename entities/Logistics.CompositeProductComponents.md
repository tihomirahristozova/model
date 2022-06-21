---
uid: Logistics.CompositeProductComponents
---
# Logistics.CompositeProductComponents Entity

**Namespace:** [Logistics](Logistics.md)  

Separate components of a product which are packaged and stored individually. Used when a single product is stored in multiple packages. Entity: Log_Composite_Product_Components (Introduced in version 23.1.0.15)

## Default Visualization
Default Display Text Format:  
_{Id}: {CompositeProductComponentId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.CompositeProductComponents](Logistics.CompositeProductComponents.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ComponentNo](Logistics.CompositeProductComponents.md#componentno) | int32 | Consecutive number of the component within this composite product. `Required` `Filter(multi eq)` 
| [ComponentProductId](Logistics.CompositeProductComponents.md#componentproductid) | guid | The product which is a component of the composite product. `Required` `Filter(multi eq)` 
| [CompositeProductId](Logistics.CompositeProductComponents.md#compositeproductid) | guid | The product of which the current component is a part. `Required` `Filter(multi eq)` 
| [DisplayText](Logistics.CompositeProductComponents.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [FromDate](Logistics.CompositeProductComponents.md#fromdate) | date __nullable__ | When set, specifies the activation date of the component for this product. `Filter(eq;ge;le)` 
| [IsActive](Logistics.CompositeProductComponents.md#isactive) | boolean | Indicates whether the component is currently active for this composite product. `Required` `Default(true)` `Filter(eq)` 
| [Notes](Logistics.CompositeProductComponents.md#notes) | string (max) __nullable__ | Notes for this composite product component. 
| [ObjectVersion](Logistics.CompositeProductComponents.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [Quantity](Logistics.CompositeProductComponents.md#quantity) | decimal (12, 3) | The number of packages of this component that are needed to compose the product. `Required` `Default(1)` `Filter(multi eq;ge;le)` 
| [ToDate](Logistics.CompositeProductComponents.md#todate) | date __nullable__ | When set, specifies the de-activation date of the component for this product. `Filter(eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [GeneralProducts<br />CompositeProduct<br />Component](Logistics.CompositeProductComponents.md#generalproductscompositeproductcomponent) | [Products](General.Products.Products.md) |  |


## Attribute Details

### ComponentNo

Consecutive number of the component within this composite product. `Required` `Filter(multi eq)`

_Type_: **int32**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ComponentProductId

The product which is a component of the composite product. `Required` `Filter(multi eq)`

_Type_: **guid**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### CompositeProductId

The product of which the current component is a part. `Required` `Filter(multi eq)`

_Type_: **guid**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### FromDate

When set, specifies the activation date of the component for this product. `Filter(eq;ge;le)`

_Type_: **date __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### IsActive

Indicates whether the component is currently active for this composite product. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Category_: **System**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

Notes for this composite product component.

_Type_: **string (max) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Quantity

The number of packages of this component that are needed to compose the product. `Required` `Default(1)` `Filter(multi eq;ge;le)`

_Type_: **decimal (12, 3)**  
_Category_: **System**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### ToDate

When set, specifies the de-activation date of the component for this product. `Filter(eq;ge;le)`

_Type_: **date __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### GeneralProductsCompositeProductComponent

_Type_: **[Products](General.Products.Products.md)**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


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

[!list limit=1000 erp.entity=Logistics.CompositeProductComponents erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.CompositeProductComponents erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_CompositeProductComponents?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_CompositeProductComponents?$top=10>

