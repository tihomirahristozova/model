---
uid: Applications.Rental.AssetTypeProperties
---
# Applications.Rental.AssetTypeProperties

Contains the properties, which are required for each asset category. Entity: Rent_Asset_Type_Properties

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Rental.AssetTypeProperties.md#Id) | guid |  
| [DefaultValue](Applications.Rental.AssetTypeProperties.md#DefaultValue) | string (nullable) | The default value of the property. [Filter(like)] 
| [DefaultValueId](Applications.Rental.AssetTypeProperties.md#DefaultValueId) | guid (nullable) | The value id of the default value of the property. [Filter(multi eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Property](Applications.Rental.AssetTypeProperties.md#Property) | [General.CustomProperties](General.CustomProperties.md) | The user-defined property, which is required for assets of the specified type. [Required] [Filter(multi eq)] |
| [RentalAssetType](Applications.Rental.AssetTypeProperties.md#RentalAssetType) | [Applications.Rental.AssetTypes](Applications.Rental.AssetTypes.md) | The [AssetType](Applications.Rental.AssetTypes.md) to which this AssetTypeProperty belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DefaultValue

> The default value of the property. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### DefaultValueId

> The value id of the default value of the property. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### Property

> The user-defined property, which is required for assets of the specified type. [Required] [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RentalAssetType

> The [AssetType](Applications.Rental.AssetTypes.md) to which this AssetTypeProperty belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Rental.AssetTypes](Applications.Rental.AssetTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Rental.AssetTypeProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Rental.AssetTypeProperties erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Rental.AssetTypeProperties erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_AssetTypeProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_AssetTypeProperties?$top=10>

