# General.CustomProperties

User-defined properties, which can supplement the system properties of almost all entities in the system. Entity: Gen_Properties

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.CustomProperties.md#Id) | guid |  
| [AllowedValuesEntityName](General.CustomProperties.md#AllowedValuesEntityName) | string (nullable) | When not null, specifies that the allowed values are retrieved from the specified entity. [Filter(eq)] 
| [AllowedValuesFilterXML](General.CustomProperties.md#AllowedValuesFilterXML) | string (nullable) | When not null specifies the filter to apply when extracting allowed values from entity. 
| [EntityName](General.CustomProperties.md#EntityName) | string | The entity for which the property is applicable. [Required] [Filter(eq)] [ORD] 
| [Hint](General.CustomProperties.md#Hint) | [MultilanguageString](../data-types/MultilanguageString.md) (nullable) | The hint, which is displayed alongside the property. [Filter(multi eq;like)] (Introduced in version 20.1.100.0) 
| [KeyOrder](General.CustomProperties.md#KeyOrder) | byte (nullable) | When not null, indicates, that the property is a key property and contains the property consequtive position withing the entity. Used for BI and other analysis. 
| [LimitToAllowedValues](General.CustomProperties.md#LimitToAllowedValues) | boolean | When true, allows the property to be set only to allowed value. When false, the property can have any value. [Required] [Default(false)] [Filter(eq)] 
| [MaskLength](General.CustomProperties.md#MaskLength) | int16 (nullable) | Limits te length of the property value to the specified number of characters. Null means no limitation. 
| [Notes](General.CustomProperties.md#Notes) | string (nullable) | Notes for this CustomProperty. (Introduced in version 20.1.100.0) 
| [Code](General.CustomProperties.md#Code) | string | Unique property code. [Required] [Filter(multi eq;like)] [ORD] 
| [Name](General.CustomProperties.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | The name of this CustomProperty. [Required] [Filter(like)] [ORD] 
| [PropertyType](General.CustomProperties.md#PropertyType) | [General.CustomPropertiesRepository.PropertyType](General.CustomProperties.md#PropertyType) | Type of property values. 'T' - text; 'P' - picture; 'N' - number; 'D' - date. [Required] [Default("T")] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AllowedValuesParentProperty](General.CustomProperties.md#AllowedValuesParentProperty) | [General.CustomProperties](General.CustomProperties.md) (nullable) | Specifies the user defined property, which is used for filtering the allowed values by value of the parent property. [Filter(multi eq)] |
| [AllowedValuesProperty](General.CustomProperties.md#AllowedValuesProperty) | [General.CustomProperties](General.CustomProperties.md) (nullable) | When not null, specifies that the current property can have the same allowed values as the specified property. Also, this makes the current and the specified property copy-compatible. [Filter(multi eq)] |
| [PropertiesCategory](General.CustomProperties.md#PropertiesCategory) | [General.PropertiesCategories](General.PropertiesCategories.md) (nullable) | When not null, categorizes the property under a category. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| AllowedValues | [General.CustomPropertyAllowedValues](General.CustomPropertyAllowedValues.md) | List of [CustomPropertyAllowedValue](General.CustomPropertyAllowedValues.md) child objects, based on the [General.CustomPropertyAllowedValue.Property](General.CustomPropertyAllowedValues.md#Property) back reference 
| EnterpriseCompanyFilters | [General.PropertyEnterpriseCompanyFilters](General.PropertyEnterpriseCompanyFilters.md) | List of [PropertyEnterpriseCompanyFilter](General.PropertyEnterpriseCompanyFilters.md) child objects, based on the [General.PropertyEnterpriseCompanyFilter.Property](General.PropertyEnterpriseCompanyFilters.md#Property) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AllowedValuesEntityName

> When not null, specifies that the allowed values are retrieved from the specified entity. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### AllowedValuesFilterXML

> When not null specifies the filter to apply when extracting allowed values from entity.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### EntityName

> The entity for which the property is applicable. [Required] [Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### Hint

> The hint, which is displayed alongside the property. [Filter(multi eq;like)] (Introduced in version 20.1.100.0)

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md) (nullable)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### KeyOrder

> When not null, indicates, that the property is a key property and contains the property consequtive position withing the entity. Used for BI and other analysis.

_Type_: **byte (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LimitToAllowedValues

> When true, allows the property to be set only to allowed value. When false, the property can have any value. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### MaskLength

> Limits te length of the property value to the specified number of characters. Null means no limitation.

_Type_: **int16 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

> Notes for this CustomProperty. (Introduced in version 20.1.100.0)

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Code

> Unique property code. [Required] [Filter(multi eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  

### Name

> The name of this CustomProperty. [Required] [Filter(like)] [ORD]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  

### PropertyType

> Type of property values. 'T' - text; 'P' - picture; 'N' - number; 'D' - date. [Required] [Default("T")]

_Type_: **[General.CustomPropertiesRepository.PropertyType](General.CustomProperties.md#PropertyType)**  
Allowed values for the [PropertyType](General.CustomProperties.md#PropertyType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Text | Text value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Text' |
| Number | Number value. Stored as 'N'. <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Number' |
| Picture | Picture value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Picture' |
| Date | Date value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Date' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Text**  


## Reference Details

### AllowedValuesParentProperty

> Specifies the user defined property, which is used for filtering the allowed values by value of the parent property. [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### AllowedValuesProperty

> When not null, specifies that the current property can have the same allowed values as the specified property. Also, this makes the current and the specified property copy-compatible. [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PropertiesCategory

> When not null, categorizes the property under a category. [Filter(multi eq)]

_Type_: **[General.PropertiesCategories](General.PropertiesCategories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.CustomProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.CustomProperties erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.CustomProperties erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_CustomProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_CustomProperties?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Properties?$top=10>

