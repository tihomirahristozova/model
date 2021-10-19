---
uid: Applications.Rental.AssetTypeProperties
---
# Applications.Rental.AssetTypeProperties Entity

**Namespace:** [Applications.Rental](Applications.Rental.md)  

Contains the properties, which are required for each asset category. Entity: Rent_Asset_Type_Properties

## Default Visualization
Default Display Text Format:  
_{RentalAssetType.RentalAssetTypeName}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Rental.AssetTypes](Applications.Rental.AssetTypes.md)  
Aggregate Root:  
[Applications.Rental.AssetTypes](Applications.Rental.AssetTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultValue](Applications.Rental.AssetTypeProperties.md#defaultvalue) | string (254) __nullable__ | The default value of the property. `Filter(like)` 
| [DefaultValueId](Applications.Rental.AssetTypeProperties.md#defaultvalueid) | guid __nullable__ | The value id of the default value of the property. `Filter(multi eq)` 
| [Id](Applications.Rental.AssetTypeProperties.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Property](Applications.Rental.AssetTypeProperties.md#property) | [CustomProperties](General.CustomProperties.md) | The user-defined property, which is required for assets of the specified type. `Required` `Filter(multi eq)` |
| [RentalAssetType](Applications.Rental.AssetTypeProperties.md#rentalassettype) | [AssetTypes](Applications.Rental.AssetTypes.md) | The `AssetType`(Applications.Rental.AssetTypes.md) to which this AssetTypeProperty belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### DefaultValue

The default value of the property. `Filter(like)`

_Type_: **string (254) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### DefaultValueId

The value id of the default value of the property. `Filter(multi eq)`

_Type_: **guid __nullable__**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Property

The user-defined property, which is required for assets of the specified type. `Required` `Filter(multi eq)`

_Type_: **[CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### RentalAssetType

The `AssetType`(Applications.Rental.AssetTypes.md) to which this AssetTypeProperty belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[AssetTypes](Applications.Rental.AssetTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Applications.Rental.AssetTypeProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Rental.AssetTypeProperties erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_AssetTypeProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_AssetTypeProperties?$top=10>

