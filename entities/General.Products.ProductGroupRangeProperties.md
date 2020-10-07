# General.Products.ProductGroupRangeProperties

When specified for a product group, provides a way for automatical creation of new products, based on altering a set of values of some user-defined properties. Each value combination is used to create a new, unique product within the group. Entity: Gen_Product_Group_Range_Properties

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Products.ProductGroupRangeProperties.md#Id) | guid |  
| [FromPropertyValue](General.Products.ProductGroupRangeProperties.md#FromPropertyValue) | string (nullable) | Starting value of the range of alternative values. Used only when Rage Type = R (range). 
| [PropertyValuesList](General.Products.ProductGroupRangeProperties.md#PropertyValuesList) | string (nullable) | Contains the enumeration of all values in the alternating value set. Used only when Rage Type = E (enumeratio). 
| [RangeType](General.Products.ProductGroupRangeProperties.md#RangeType) | [General.Products.ProductGroupRangePropertiesRepository.RangeType](General.Products.ProductGroupRangeProperties.md#RangeType) | Specifies the method of the creation of the value set: R - by range from-to; E - by enumeration of all values;. [Required] [Default("R")] 
| [ToPropertyValue](General.Products.ProductGroupRangeProperties.md#ToPropertyValue) | string (nullable) | Ending value of the range of alternative values. Used only when Rage Type = R (range). 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProductGroup](General.Products.ProductGroupRangeProperties.md#ProductGroup) | [General.Products.ProductGroups](General.Products.ProductGroups.md) | The [ProductGroup](General.Products.ProductGroupRangeProperties.md#ProductGroup) to which this ProductGroupRangeProperty belongs. [Required] [Filter(multi eq)] [Owner] |
| [Property](General.Products.ProductGroupRangeProperties.md#Property) | [General.CustomProperties](General.CustomProperties.md) | The property whose values will be altered. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FromPropertyValue

> Starting value of the range of alternative values. Used only when Rage Type = R (range).

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PropertyValuesList

> Contains the enumeration of all values in the alternating value set. Used only when Rage Type = E (enumeratio).

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RangeType

> Specifies the method of the creation of the value set: R - by range from-to; E - by enumeration of all values;. [Required] [Default("R")]

_Type_: **[General.Products.ProductGroupRangePropertiesRepository.RangeType](General.Products.ProductGroupRangeProperties.md#RangeType)**  
Allowed values for the [RangeType](General.Products.ProductGroupRangeProperties.md#RangeType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Range | Range value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Range' |
| List | List value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'List' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Range**  

### ToPropertyValue

> Ending value of the range of alternative values. Used only when Rage Type = R (range).

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ProductGroup

> The [ProductGroup](General.Products.ProductGroupRangeProperties.md#ProductGroup) to which this ProductGroupRangeProperty belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Products.ProductGroups](General.Products.ProductGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Property

> The property whose values will be altered. [Required] [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Products.ProductGroupRangeProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.ProductGroupRangeProperties erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Products.ProductGroupRangeProperties erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductGroupRangeProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductGroupRangeProperties?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Product_Group_Range_Properties?$top=10>

