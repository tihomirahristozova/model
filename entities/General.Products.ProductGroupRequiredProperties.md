---
uid: General.Products.ProductGroupRequiredProperties
---
# General.Products.ProductGroupRequiredProperties Entity

**Namespace:** [General.Products](General.Products.md)  

Contains the properties, that are required to be set, when creating new products in the category and its sub-categories. Entity: Gen_Product_Group_Required_Properties

## Default Visualization
Default Display Text Format:  
_{ProductGroup.NextPartNumber}: {ProductGroup.Name:T}_  
Default Search Member:  
_ProductGroup.NextPartNumber_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Products.ProductGroups](General.Products.ProductGroups.md)  
Aggregate Root:  
[General.Products.ProductGroups](General.Products.ProductGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultPropertyValue](General.Products.ProductGroupRequiredProperties.md#defaultpropertyvalue) | string (nullable) | When not null, specifies the default value of the property, for new products in the group. 
| [DefaultProperty<br />ValueDescription](General.Products.ProductGroupRequiredProperties.md#defaultpropertyvaluedescription) | string (nullable) | When not null, specifies the default description value of the property, for new products in the group. 
| [DefaultValueId](General.Products.ProductGroupRequiredProperties.md#defaultvalueid) | guid (nullable) | When not null, specifies the default internal Id value of the property, for new products in the group. `Filter(multi eq)` 
| [Id](General.Products.ProductGroupRequiredProperties.md#id) | guid |  
| [PropertyNo](General.Products.ProductGroupRequiredProperties.md#propertyno) | int32 | The consecutive number (position) of the property within the product group and its subgroups. The parent groups of each leaf group should contain only unique property numbers. `Required` `Default(0)` 
| [Required](General.Products.ProductGroupRequiredProperties.md#required) | boolean | Specifies whether the property is required (or only suggested) to be set for new products. Suggested properties are used by product configuration and other product creation services. true=Required, false=Suggested. `Required` `Default(false)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProductGroup](General.Products.ProductGroupRequiredProperties.md#productgroup) | [ProductGroups](General.Products.ProductGroups.md) | The `ProductGroup`(General.Products.ProductGroupRequired<br />Properties.md#productgroup) to which this ProductGroupRequired<br />Property belongs. `Required` `Filter(multi eq)` `Owner` |
| [Property](General.Products.ProductGroupRequiredProperties.md#property) | [CustomProperties](General.CustomProperties.md) | The property, that is required when creating new products in the group. The property is automatically added to new products, created in the group. The property should be with Entity Type = 'Product'. `Required` `Filter(multi eq)` |


## Attribute Details

### DefaultPropertyValue

When not null, specifies the default value of the property, for new products in the group.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultPropertyValueDescription

When not null, specifies the default description value of the property, for new products in the group.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultValueId

When not null, specifies the default internal Id value of the property, for new products in the group. `Filter(multi eq)`

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### PropertyNo

The consecutive number (position) of the property within the product group and its subgroups. The parent groups of each leaf group should contain only unique property numbers. `Required` `Default(0)`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Back-End Default Expression:_  
`( obj.ProductGroup.RequiredProperties.Select( c => c.PropertyNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.ProductGroup.RequiredProperties.Select( c => c.PropertyNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Required

Specifies whether the property is required (or only suggested) to be set for new products. Suggested properties are used by product configuration and other product creation services. true=Required, false=Suggested. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### ProductGroup

The `ProductGroup`(General.Products.ProductGroupRequiredProperties.md#productgroup) to which this ProductGroupRequiredProperty belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ProductGroups](General.Products.ProductGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Property

The property, that is required when creating new products in the group. The property is automatically added to new products, created in the group. The property should be with Entity Type = 'Product'. `Required` `Filter(multi eq)`

_Type_: **[CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Products.ProductGroupRequiredProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.ProductGroupRequiredProperties erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductGroupRequiredProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductGroupRequiredProperties?$top=10>

