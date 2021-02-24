---
uid: General.Products.ProductGroups
---
# General.Products.ProductGroups Entity

**Namespace:** [General.Products](General.Products.md)  

Hierarchical categorization of the products. Entity: Gen_Product_Groups

## Default Visualization
Default Display Text Format:  
_{NextPartNumber}: {Name:T}_  
Default Search Member:  
_NextPartNumber_  

## Aggregate
  @aggregates  
Aggregate Tree  
* [General.Products.ProductGroups](General.Products.ProductGroups.md)  
  * [General.Products.ProductGroupRangeProperties](General.Products.ProductGroupRangeProperties.md)  
  * [General.Products.ProductGroupRequiredProperties](General.Products.ProductGroupRequiredProperties.md)  
  * [Production.Technologies.PrincipalRecipes](Production.Technologies.PrincipalRecipes.md)  
    * [Production.Technologies.PrincipalRecipeIngredients](Production.Technologies.PrincipalRecipeIngredients.md)  
    * [Production.Technologies.PrincipalRecipeOperations](Production.Technologies.PrincipalRecipeOperations.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Active](General.Products.ProductGroups.md#active) | boolean | True if the product group is active, false - not to list in combo boxes for choosing in new documents. [Required] [Default(true)] [Filter(eq)] 
| [Code](General.Products.ProductGroups.md#code) | string | The unique code of the ProductGroup. [Required] [Filter(eq;like)] [ORD] 
| [ConfiguratorCreatesRecipe](General.Products.ProductGroups.md#configuratorcreatesrecipe) | boolean | Whether the product configurator should create one default recipe. true=yes;false=no. [Required] [Default(false)] 
| [ConfiguratorStatus](General.Products.ProductGroups.md#configuratorstatus) | [ConfiguratorStatus](General.Products.ProductGroups.md#configuratorstatus) | Usage of product configurator for new products. 0=Product configurator cannot be used to create products in this group;1=The configurator can be used;2=The configurator should be used and products cannot be created directly. [Required] [Default(0)] 
| [FullPath](General.Products.ProductGroups.md#fullpath) | string | Full tree path in the form /parent/.../leaf/. Contains the group names. [Required] [Default("")] [Filter(eq;like)] [ORD] 
| [Id](General.Products.ProductGroups.md#id) | guid |  
| [Name](General.Products.ProductGroups.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Group name should be unique among the other groups within the same parent. [Required] [Filter(eq;like)] 
| [NextPartNumber](General.Products.ProductGroups.md#nextpartnumber) | string (nullable) | Contains the next part number to be auto-assigned to parts, created in the group or sub-groups. 
| [NextSerialNumber](General.Products.ProductGroups.md#nextserialnumber) | string (nullable) | When not null, specifies the next serial number, that should be assigned to new produced items. [Filter(eq;like)] 
| [Notes](General.Products.ProductGroups.md#notes) | string (nullable) | User notes for the item group. 
| [Parent](General.Products.ProductGroups.md#parent) | string | Full tree path of the parent group in the form /parent/.../leaf/. Contains the group names. [Required] [Default("/")] [Filter(eq)] [ORD] 
| [Picture](General.Products.ProductGroups.md#picture) | byte[] (nullable) | The picture of the product group. 
| [PictureLastUpdateTime](General.Products.ProductGroups.md#picturelastupdatetime) | datetime (nullable) | Last update time of the Picture. [Filter(ge;le)] [ReadOnly] 
| [ProductDescriptionMask](General.Products.ProductGroups.md#productdescriptionmask) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | When not null specifies mask for new product descriptions for this group and its sub-groups. The mask substitutes {0}..{n} with the appropriate custom attributes. 
| [ProductNameMask](General.Products.ProductGroups.md#productnamemask) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | When not null specifies mask for new product names for this group and its sub-groups. The mask substitutes {0}..{n} with the appropriate custom attributes. 
| [UseLots](General.Products.ProductGroups.md#uselots) | [UseLots](General.Products.ProductGroups.md#uselots) (nullable) | Specifies whether for the products from this group and its sub-groups the use of lots in store documents is required or is unallowed or is allowed while not required. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultMeasurementUnit](General.Products.ProductGroups.md#defaultmeasurementunit) | [MeasurementUnits](General.MeasurementUnits.md) (nullable) | When not null, specifies default measurement unit, which should be assigned to new products in the group. [Filter(multi eq)] |
| [DefaultProductType](General.Products.ProductGroups.md#defaultproducttype) | [ProductTypes](General.Products.ProductTypes.md) (nullable) | When not null, specifies default product type, which should be assigned to new products in the group. [Filter(multi eq)] |
| [EnterpriseCompany](General.Products.ProductGroups.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | When not null, specifies that the product group, its sub-groups and products are specific to a given enterprise company and may be used only in documents from this enterprise company. [Filter(multi eq)] |
| [PricingModel](General.Products.ProductGroups.md#pricingmodel) | [PricingModels](Crm.Pricing.PricingModels.md) (nullable) | When not null, specifies the pricing model, for the products in this product group. The model is by default valid also for sub-groups, unless they have other models. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| PrincipalRecipes | [PrincipalRecipes](Production.Technologies.PrincipalRecipes.md) | List of [PrincipalRecipe](Production.Technologies.PrincipalRecipes.md) child objects, based on the [Production.Technologies.PrincipalRecipe.ProductGroup](Production.Technologies.PrincipalRecipes.md#productgroup) back reference 
| RangeProperties | [ProductGroupRangeProperties](General.Products.ProductGroupRangeProperties.md) | List of [ProductGroupRange<br />Property](General.Products.ProductGroupRange<br />Properties.md) child objects, based on the [General.Products.ProductGroupRangeProperty.ProductGroup](General.Products.ProductGroupRange<br />Properties.md#productgroup) back reference 
| RequiredProperties | [ProductGroupRequiredProperties](General.Products.ProductGroupRequiredProperties.md) | List of [ProductGroupRequired<br />Property](General.Products.ProductGroupRequired<br />Properties.md) child objects, based on the [General.Products.ProductGroupRequired<br />Property.ProductGroup](General.Products.ProductGroupRequired<br />Properties.md#productgroup) back reference 


## Attribute Details

### Active

True if the product group is active, false - not to list in combo boxes for choosing in new documents. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Code

The unique code of the ProductGroup. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### ConfiguratorCreatesRecipe

Whether the product configurator should create one default recipe. true=yes;false=no. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ConfiguratorStatus

Usage of product configurator for new products. 0=Product configurator cannot be used to create products in this group;1=The configurator can be used;2=The configurator should be used and products cannot be created directly. [Required] [Default(0)]

_Type_: **[ConfiguratorStatus](General.Products.ProductGroups.md#configuratorstatus)**  
Allowed values for the [ConfiguratorStatus](General.Products.ProductGroups.md#configuratorstatus) data attribute  
_Allowed Values (General.Products.ProductGroupsRepository.ConfiguratorStatus Enum Members)_  

| Value | Description |
| ---- | --- |
| NotAllowed | NotAllowed value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NotAllowed' |
| Allowed | Allowed value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Allowed' |
| Obligatory | Obligatory value. Stored as 2. <br /> _Database Value:_ 2 <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Obligatory' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### FullPath

Full tree path in the form /parent/.../leaf/. Contains the group names. [Required] [Default("")] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Default Value_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Group name should be unique among the other groups within the same parent. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### NextPartNumber

Contains the next part number to be auto-assigned to parts, created in the group or sub-groups.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### NextSerialNumber

When not null, specifies the next serial number, that should be assigned to new produced items. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

User notes for the item group.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Parent

Full tree path of the parent group in the form /parent/.../leaf/. Contains the group names. [Required] [Default("/")] [Filter(eq)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Default Value_: **/**  

### Picture

The picture of the product group.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PictureLastUpdateTime

Last update time of the Picture. [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ProductDescriptionMask

When not null specifies mask for new product descriptions for this group and its sub-groups. The mask substitutes {0}..{n} with the appropriate custom attributes.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProductNameMask

When not null specifies mask for new product names for this group and its sub-groups. The mask substitutes {0}..{n} with the appropriate custom attributes.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UseLots

Specifies whether for the products from this group and its sub-groups the use of lots in store documents is required or is unallowed or is allowed while not required.

_Type_: **[UseLots](General.Products.ProductGroups.md#uselots) (nullable)**  
Allowed values for the [UseLots](General.Products.ProductGroups.md#uselots) data attribute  
_Allowed Values (General.Products.ProductGroupsRepository.UseLots Enum Members)_  

| Value | Description |
| ---- | --- |
| Allowed | Allowed value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Allowed' |
| NotAllowed | NotAllowed value. Stored as 'N'. <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NotAllowed' |
| Required | Required value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Required' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### DefaultMeasurementUnit

When not null, specifies default measurement unit, which should be assigned to new products in the group. [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DefaultProductType

When not null, specifies default product type, which should be assigned to new products in the group. [Filter(multi eq)]

_Type_: **[ProductTypes](General.Products.ProductTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

When not null, specifies that the product group, its sub-groups and products are specific to a given enterprise company and may be used only in documents from this enterprise company. [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PricingModel

When not null, specifies the pricing model, for the products in this product group. The model is by default valid also for sub-groups, unless they have other models. [Filter(multi eq)]

_Type_: **[PricingModels](Crm.Pricing.PricingModels.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Products.ProductGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.ProductGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductGroups?$top=10>

