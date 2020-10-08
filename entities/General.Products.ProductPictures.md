---
uid: General.Products.ProductPictures
---
# General.Products.ProductPictures

Pictures of products. Entity: Gen_Product_Pictures

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Products.ProductPictures.md#Id) | guid |  
| [Comments](General.Products.ProductPictures.md#Comments) | string (nullable) | Comments for this ProductPicture. 
| [IsDefault](General.Products.ProductPictures.md#IsDefault) | boolean | True=This is the default picture for the product and the size class; false=otherwise. [Required] [Default(false)] [Filter(eq)] 
| [LastUpdateTime](General.Products.ProductPictures.md#LastUpdateTime) | datetime (nullable) | The exact server time, when the picture was last updated. Set automatically. [Filter(ge;le)] [ReadOnly] 
| [Picture](General.Products.ProductPictures.md#Picture) | byte[] (nullable) | The actual product picture. Can be null if we insert only some comments. 
| [PictureNo](General.Products.ProductPictures.md#PictureNo) | int32 | Unique picture number within the product. Also used for sorting. [Required] [Filter(eq;like)] 
| [PictureSizeClass](General.Products.ProductPictures.md#PictureSizeClass) | [General.Products.ProductPicturesRepository.PictureSizeClass](General.Products.ProductPictures.md#PictureSizeClass) (nullable) | Specifies the relative picture size and usage. S=Small picture (thumbnail), L=Large picture (full size), null=unspecified. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Product](General.Products.ProductPictures.md#Product) | [General.Products.Products](General.Products.Products.md) | The [Product](General.Products.ProductPictures.md#Product) to which this ProductPicture belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Comments

> Comments for this ProductPicture.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsDefault

> True=This is the default picture for the product and the size class; false=otherwise. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

_Front-End Recalc Expressions:_  
`(obj.Product.Pictures.Take(1).Count() == 0)`
### LastUpdateTime

> The exact server time, when the picture was last updated. Set automatically. [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Picture

> The actual product picture. Can be null if we insert only some comments.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PictureNo

> Unique picture number within the product. Also used for sorting. [Required] [Filter(eq;like)]

_Type_: **int32**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.Product.Pictures.Select(c => c.PictureNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.Product.Pictures.Select(c => c.PictureNo).DefaultIfEmpty(0).Max() + 10)`
### PictureSizeClass

> Specifies the relative picture size and usage. S=Small picture (thumbnail), L=Large picture (full size), null=unspecified.

_Type_: **[General.Products.ProductPicturesRepository.PictureSizeClass](General.Products.ProductPictures.md#PictureSizeClass) (nullable)**  
Allowed values for the [PictureSizeClass](General.Products.ProductPictures.md#PictureSizeClass) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| SmallPictureThumbnail | SmallPictureThumbnail value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'SmallPictureThumbnail' |
| LargePictureFullSize | LargePictureFullSize value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'LargePictureFullSize' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Product

> The [Product](General.Products.ProductPictures.md#Product) to which this ProductPicture belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Products.ProductPictures erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.ProductPictures erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Products.ProductPictures erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductPictures?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductPictures?$top=10>

