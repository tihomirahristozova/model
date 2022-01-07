---
uid: General.Products.ProductDocumentAmounts
---
# General.Products.ProductDocumentAmounts Entity

**Namespace:** [General.Products](General.Products.md)  

Contains custom percent ratios for additional amount distribution over products. Entity: Gen_Product_Document_Amounts

## Default Visualization
Default Display Text Format:  
_{Product.Name:T}_  
Default Search Members:  
_Product.Name_  
Name Data Member:  
_Product.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Products.Products](General.Products.Products.md)  
Aggregate Root:  
[General.Products.Products](General.Products.Products.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](General.Products.ProductDocumentAmounts.md#displaytext) | string |  
| [Id](General.Products.ProductDocumentAmounts.md#id) | guid |  
| [LinePercent](General.Products.ProductDocumentAmounts.md#linepercent) | decimal (14, 3) | The custom percent for the current product and amount type. `Required` `Default(0)` 
| [ObjectVersion](General.Products.ProductDocumentAmounts.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentAmountType](General.Products.ProductDocumentAmounts.md#documentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) | The amount type for which the custom percent is defined. `Required` `Filter(multi eq)` |
| [Product](General.Products.ProductDocumentAmounts.md#product) | [Products](General.Products.Products.md) | The <see cref="Product"/> to which this ProductDocumentAmount belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### DisplayText

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LinePercent

The custom percent for the current product and amount type. `Required` `Default(0)`

_Type_: **decimal (14, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### DocumentAmountType

The amount type for which the custom percent is defined. `Required` `Filter(multi eq)`

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The <see cref="Product"/> to which this ProductDocumentAmount belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Products](General.Products.Products.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  


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

[!list limit=1000 erp.entity=General.Products.ProductDocumentAmounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Products.ProductDocumentAmounts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductDocumentAmounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductDocumentAmounts?$top=10>

