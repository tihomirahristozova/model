---
uid: Applications.Cms.ProductCatalogWebModules
---
# Applications.Cms.ProductCatalogWebModules Entity

**Namespace:** [Applications.Cms](Applications.Cms.md)  
**Inherited From:** [Applications.Cms.WebModules](Applications.Cms.WebModules.md)  

A web module, which presents a whole product catalog. Entity: Cms_Product_Catalog_Web_Modules

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Cms.WebSites](Applications.Cms.WebSites.md)  
Aggregate Root:  
[Applications.Cms.WebSites](Applications.Cms.WebSites.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Cms.ProductCatalogWebModules.md#id) | guid |  
| [IsPublished](Applications.Cms.ProductCatalogWebModules.md#ispublished) | boolean | Specifies whether the module is published and will be showed in the web site. `Required` `Default(false)` `Filter(eq)` (Inherited from [WebModules](Applications.Cms.WebModules.md)) 
| [LocalUrl](Applications.Cms.ProductCatalogWebModules.md#localurl) | string (128) __nullable__ | The local Module Url. The full Url of a module is formed based on the sites Base Url, the local Urls of all parent modules and the module Local Url. Null means that the web Module is the default web module within the parent path. `Filter(like)` (Inherited from [WebModules](Applications.Cms.WebModules.md)) 
| [ModulePicture](Applications.Cms.ProductCatalogWebModules.md#modulepicture) | byte[] __nullable__ | Default picture. Used for picture links, small module icons, etc. PNG format is suggested. (Inherited from [WebModules](Applications.Cms.WebModules.md)) 
| [ModuleType](Applications.Cms.ProductCatalogWebModules.md#moduletype) | [ModuleType](Applications.Cms.ProductCatalogWebModules.md#moduletype) | Specifies the content handler. The content handler is responsible for generating the actual web page content. Module Types include Category, Static, News, Product, etc. `Required` `Filter(like)` (Inherited from [WebModules](Applications.Cms.WebModules.md)) 
| [Name](Applications.Cms.ProductCatalogWebModules.md#name) | string (512) | Multilanguage Module name. This is used as a title when displaying the web Module. `Required` `Filter(like)` (Inherited from [WebModules](Applications.Cms.WebModules.md)) 
| [ObjectVersion](Applications.Cms.ProductCatalogWebModules.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Applications.Cms.ProductCatalogWebModules.md#parent) | [WebModules](Applications.Cms.WebModules.md) (nullable) | The parent web Module. It can only be a module with Module Type = Category. Null means that the web Module is root web Module. `Filter(multi eq)` (Inherited from [WebModules](Applications.Cms.WebModules.md)) |
| [ProductCatalog](Applications.Cms.ProductCatalogWebModules.md#productcatalog) | [ProductCatalogs](General.ProductCatalogs.md) | The product catalog, which is represented by this web module. `Required` `Filter(multi eq)` |
| [WebSite](Applications.Cms.ProductCatalogWebModules.md#website) | [WebSites](Applications.Cms.WebSites.md) | The web site to which the module belongs. `Required` `Filter(multi eq)` `Owner` (Inherited from [WebModules](Applications.Cms.WebModules.md)) |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsPublished

Specifies whether the module is published and will be showed in the web site. `Required` `Default(false)` `Filter(eq)` (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LocalUrl

The local Module Url. The full Url of a module is formed based on the sites Base Url, the local Urls of all parent modules and the module Local Url. Null means that the web Module is the default web module within the parent path. `Filter(like)` (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **string (128) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### ModulePicture

Default picture. Used for picture links, small module icons, etc. PNG format is suggested. (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **byte[] __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ModuleType

Specifies the content handler. The content handler is responsible for generating the actual web page content. Module Types include Category, Static, News, Product, etc. `Required` `Filter(like)` (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **[ModuleType](Applications.Cms.ProductCatalogWebModules.md#moduletype)**  
Allowed values for the ModuleType data attribute  
_Allowed Values (Applications.Cms.WebModulesRepository.ModuleType Enum Members)_  

| Value | Description |
| ---- | --- |
| CategoryPage | CategoryPage value. Stored as 'CAT'. <br /> _Database Value:_ 'CAT' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'CategoryPage' |
| Static | Static value. Stored as 'STA'. <br /> _Database Value:_ 'STA' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Static' |
| News | News value. Stored as 'NEW'. <br /> _Database Value:_ 'NEW' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'News' |

_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Name

Multilanguage Module name. This is used as a title when displaying the web Module. `Required` `Filter(like)` (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **string (512)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **512**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### Parent

The parent web Module. It can only be a module with Module Type = Category. Null means that the web Module is root web Module. `Filter(multi eq)` (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **[WebModules](Applications.Cms.WebModules.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductCatalog

The product catalog, which is represented by this web module. `Required` `Filter(multi eq)`

_Type_: **[ProductCatalogs](General.ProductCatalogs.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WebSite

The web site to which the module belongs. `Required` `Filter(multi eq)` `Owner` (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **[WebSites](Applications.Cms.WebSites.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources does not support ordering.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description  
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

[!list limit=1000 erp.entity=Applications.Cms.ProductCatalogWebModules erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Cms.ProductCatalogWebModules erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Cms_ProductCatalogWebModules?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Cms_ProductCatalogWebModules?$top=10>

