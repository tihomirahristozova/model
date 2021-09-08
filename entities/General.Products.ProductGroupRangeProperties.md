---
uid: General.Products.ProductGroupRangeProperties
---
# General.Products.ProductGroupRangeProperties Entity

**Namespace:** [General.Products](General.Products.md)  

When specified for a product group, provides a way for automatical creation of new products, based on altering a set of values of some user-defined properties. Each value combination is used to create a new, unique product within the group. Entity: Gen_Product_Group_Range_Properties

## Default Visualization
Default Display Text Format:  
_{ProductGroup.Name:T} #{ProductGroup.NextPartNumber}_  
Default Search Member:  
_ProductGroup.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Products.ProductGroups](General.Products.ProductGroups.md)  
Aggregate Root:  
[General.Products.ProductGroups](General.Products.ProductGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FromPropertyValue](General.Products.ProductGroupRangeProperties.md#frompropertyvalue) | string (254) __nullable__ | Starting value of the range of alternative values. Used only when Rage Type = R (range). 
| [Id](General.Products.ProductGroupRangeProperties.md#id) | guid |  
| [PropertyValuesList](General.Products.ProductGroupRangeProperties.md#propertyvalueslist) | string (max) __nullable__ | Contains the enumeration of all values in the alternating value set. Used only when Rage Type = E (enumeratio). 
| [RangeType](General.Products.ProductGroupRangeProperties.md#rangetype) | [RangeType](General.Products.ProductGroupRangeProperties.md#rangetype) | Specifies the method of the creation of the value set: R - by range from-to; E - by enumeration of all values;. `Required` `Default("R")` 
| [ToPropertyValue](General.Products.ProductGroupRangeProperties.md#topropertyvalue) | string (254) __nullable__ | Ending value of the range of alternative values. Used only when Rage Type = R (range). 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProductGroup](General.Products.ProductGroupRangeProperties.md#productgroup) | [ProductGroups](General.Products.ProductGroups.md) | The `ProductGroup`(General.Products.ProductGroupRange<br />Properties.md#productgroup) to which this ProductGroupRangeProperty belongs. `Required` `Filter(multi eq)` `Owner` |
| [Property](General.Products.ProductGroupRangeProperties.md#property) | [CustomProperties](General.CustomProperties.md) | The property whose values will be altered. `Required` `Filter(multi eq)` |


## Attribute Details

### FromPropertyValue

Starting value of the range of alternative values. Used only when Rage Type = R (range).

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### PropertyValuesList

Contains the enumeration of all values in the alternating value set. Used only when Rage Type = E (enumeratio).

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### RangeType

Specifies the method of the creation of the value set: R - by range from-to; E - by enumeration of all values;. `Required` `Default("R")`

_Type_: **[RangeType](General.Products.ProductGroupRangeProperties.md#rangetype)**  
Allowed values for the `RangeType`(General.Products.ProductGroupRangeProperties.md#rangetype) data attribute  
_Allowed Values (General.Products.ProductGroupRangePropertiesRepository.RangeType Enum Members)_  

| Value | Description |
| ---- | --- |
| Range | Range value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Range' |
| List | List value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'List' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Range**  

### ToPropertyValue

Ending value of the range of alternative values. Used only when Rage Type = R (range).

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### ProductGroup

The `ProductGroup`(General.Products.ProductGroupRangeProperties.md#productgroup) to which this ProductGroupRangeProperty belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ProductGroups](General.Products.ProductGroups.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Property

The property whose values will be altered. `Required` `Filter(multi eq)`

_Type_: **[CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.Products.ProductGroupRangeProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Products.ProductGroupRangeProperties erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductGroupRangeProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductGroupRangeProperties?$top=10>

