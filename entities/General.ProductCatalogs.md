---
uid: General.ProductCatalogs
---
# General.ProductCatalogs Entity

**Namespace:** [General](General.md)  

Product catalogs serve to organize the products for display primarily in web pages. Entity: Gen_Product_Catalogs

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.ProductCatalogs](General.ProductCatalogs.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BackgroundColor](General.ProductCatalogs.md#backgroundcolor) | int32 __nullable__ | When not null, specifies the background color to use for visualization of the catalog. The color is in RGBA color format. 
| [BackgroundImage](General.ProductCatalogs.md#backgroundimage) | byte[] __nullable__ | The background image to be used for web visualization of the catalog. null means that background image won't be displayed. 
| [BackgroundPosition<br />Horizontal](General.ProductCatalogs.md#backgroundpositionhorizontal) | [BackgroundPosition<br />Horizontal](General.ProductCatalogs.md#backgroundpositionhorizontal) | Horizontal position of the Background Image. L=Left, C=Center, R=Right. `Required` `Default("L")` 
| [BackgroundPositionVertical](General.ProductCatalogs.md#backgroundpositionvertical) | [BackgroundPositionVertical](General.ProductCatalogs.md#backgroundpositionvertical) | Vertical position of the Background Image. T=Top, C=Center, B=Bottom. `Required` `Default("T")` 
| [BackgroundRepeat](General.ProductCatalogs.md#backgroundrepeat) | [BackgroundRepeat](General.ProductCatalogs.md#backgroundrepeat) | Specifies if and how the background image will be repeated. R=Repeat both vertically and horizontally; X=Repeat only horizontally; Y=Repeat only vertically; N=No repeat. `Required` `Default("R")` 
| [Code](General.ProductCatalogs.md#code) | string (16) | Unique catalog code. `Required` 
| [FooterHtml](General.ProductCatalogs.md#footerhtml) | string (max) __nullable__ | The footer of the catalog in HTML format. Primarily used for web visualizations of the catalog. null means that there shouldn't be any user-defined footer. 
| [HeaderHtml](General.ProductCatalogs.md#headerhtml) | string (max) __nullable__ | The header of the catalog in HTML format. Primarily used for web visualizations of the catalog. null specifies that there shouldn't be any user-defined header. 
| [Id](General.ProductCatalogs.md#id) | guid |  
| [Logo](General.ProductCatalogs.md#logo) | byte[] __nullable__ | The logo of the product catalog. Used for web and other visualization of the catalog. 
| [Name](General.ProductCatalogs.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Product catalog name (multilanguage). `Required` 
| [Notes](General.ProductCatalogs.md#notes) | string (max) __nullable__ | Notes for this ProductCatalog. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [RootProductGroup](General.ProductCatalogs.md#rootproductgroup) | [ProductGroups](General.Products.ProductGroups.md) | The root (starting) product group of the catalog. Each catalog starts from a root product group and includes the products in the sub-groups. `Required` `Filter(multi eq)` |
| [WebSite](General.ProductCatalogs.md#website) | [WebSites](Systems.Core.WebSites.md) (nullable) | The ECommerce web site, which will be used to host the product catalog. When null, the product catalog would not be hosted with internal ECommerce site. `Filter(multi eq)` `Introduced in version 19.1` |


## Attribute Details

### BackgroundColor

When not null, specifies the background color to use for visualization of the catalog. The color is in RGBA color format.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### BackgroundImage

The background image to be used for web visualization of the catalog. null means that background image won't be displayed.

_Type_: **byte[] __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### BackgroundPositionHorizontal

Horizontal position of the Background Image. L=Left, C=Center, R=Right. `Required` `Default("L")`

_Type_: **[BackgroundPosition<br />Horizontal](General.ProductCatalogs.md#backgroundpositionhorizontal)**  
Allowed values for the `BackgroundPositionHorizontal`(General.ProductCatalogs.md#backgroundpositionhorizontal) data attribute  
_Allowed Values (General.ProductCatalogsRepository.BackgroundPositionHorizontal Enum Members)_  

| Value | Description |
| ---- | --- |
| Left | Left value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Left' |
| Center | Center value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Center' |
| Right | Right value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Right' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Left**  

### BackgroundPositionVertical

Vertical position of the Background Image. T=Top, C=Center, B=Bottom. `Required` `Default("T")`

_Type_: **[BackgroundPositionVertical](General.ProductCatalogs.md#backgroundpositionvertical)**  
Allowed values for the `BackgroundPositionVertical`(General.ProductCatalogs.md#backgroundpositionvertical) data attribute  
_Allowed Values (General.ProductCatalogsRepository.BackgroundPositionVertical Enum Members)_  

| Value | Description |
| ---- | --- |
| Top | Top value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Top' |
| Center | Center value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Center' |
| Bottom | Bottom value. Stored as 'B'. <br /> _Database Value:_ 'B' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Bottom' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Top**  

### BackgroundRepeat

Specifies if and how the background image will be repeated. R=Repeat both vertically and horizontally; X=Repeat only horizontally; Y=Repeat only vertically; N=No repeat. `Required` `Default("R")`

_Type_: **[BackgroundRepeat](General.ProductCatalogs.md#backgroundrepeat)**  
Allowed values for the `BackgroundRepeat`(General.ProductCatalogs.md#backgroundrepeat) data attribute  
_Allowed Values (General.ProductCatalogsRepository.BackgroundRepeat Enum Members)_  

| Value | Description |
| ---- | --- |
| RepeatBothVertically<br />AndHorizontally | RepeatBothVertically<br />AndHorizontally value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'RepeatBothVertically<br />AndHorizontally' |
| RepeatOnlyHorizontally | RepeatOnlyHorizontally value. Stored as 'X'. <br /> _Database Value:_ 'X' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'RepeatOnlyHorizontally' |
| RepeatOnlyVertically | RepeatOnlyVertically value. Stored as 'Y'. <br /> _Database Value:_ 'Y' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'RepeatOnlyVertically' |
| NoRepeat | NoRepeat value. Stored as 'N'. <br /> _Database Value:_ 'N' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'NoRepeat' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **RepeatBothVerticallyAndHorizontally**  

### Code

Unique catalog code. `Required`

_Type_: **string (16)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### FooterHtml

The footer of the catalog in HTML format. Primarily used for web visualizations of the catalog. null means that there shouldn't be any user-defined footer.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### HeaderHtml

The header of the catalog in HTML format. Primarily used for web visualizations of the catalog. null specifies that there shouldn't be any user-defined header.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Logo

The logo of the product catalog. Used for web and other visualization of the catalog.

_Type_: **byte[] __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

Product catalog name (multilanguage). `Required`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

Notes for this ProductCatalog.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### RootProductGroup

The root (starting) product group of the catalog. Each catalog starts from a root product group and includes the products in the sub-groups. `Required` `Filter(multi eq)`

_Type_: **[ProductGroups](General.Products.ProductGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WebSite

The ECommerce web site, which will be used to host the product catalog. When null, the product catalog would not be hosted with internal ECommerce site. `Filter(multi eq)` `Introduced in version 19.1`

_Type_: **[WebSites](Systems.Core.WebSites.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.ProductCatalogs erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.ProductCatalogs erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_ProductCatalogs?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_ProductCatalogs?$top=10>

