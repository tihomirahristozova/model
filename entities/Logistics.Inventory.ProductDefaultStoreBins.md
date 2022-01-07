---
uid: Logistics.Inventory.ProductDefaultStoreBins
---
# Logistics.Inventory.ProductDefaultStoreBins Entity

**Namespace:** [Logistics.Inventory](Logistics.Inventory.md)  

The default store bins in which products should be placed. Entity: Inv_Product_Default_Store_Bins

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
| [DisplayText](Logistics.Inventory.ProductDefaultStoreBins.md#displaytext) | string |  
| [Id](Logistics.Inventory.ProductDefaultStoreBins.md#id) | guid |  
| [ObjectVersion](Logistics.Inventory.ProductDefaultStoreBins.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultBin](Logistics.Inventory.ProductDefaultStoreBins.md#defaultbin) | [StoreBins](Logistics.Inventory.StoreBins.md) | The default bin, which should be used for this product. `Required` `Filter(multi eq)` |
| [Product](Logistics.Inventory.ProductDefaultStoreBins.md#product) | [Products](General.Products.Products.md) | The <see cref="General.Products.Product"/> to which this ProductDefaultStoreBin belongs. `Required` `Filter(multi eq)` `Owner` |
| [Store](Logistics.Inventory.ProductDefaultStoreBins.md#store) | [Stores](Logistics.Inventory.Stores.md) | The store, for which the default bin is specified. `Required` `Filter(multi eq)` |


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

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### DefaultBin

The default bin, which should be used for this product. `Required` `Filter(multi eq)`

_Type_: **[StoreBins](Logistics.Inventory.StoreBins.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The <see cref="General.Products.Product"/> to which this ProductDefaultStoreBin belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Products](General.Products.Products.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Store

The store, for which the default bin is specified. `Required` `Filter(multi eq)`

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
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

[!list limit=1000 erp.entity=Logistics.Inventory.ProductDefaultStoreBins erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Inventory.ProductDefaultStoreBins erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_ProductDefaultStoreBins?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_ProductDefaultStoreBins?$top=10>

