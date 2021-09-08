---
uid: General.MeasurementUnits
---
# General.MeasurementUnits Entity

**Namespace:** [General](General.md)  

Contains all measurement units, grouped in categories. Each category has one base unit (with ratio 1/1) and unlimited number of derived units with fixed ratio to the base unit. Entity: Gen_Measurement_Units

## Default Visualization
Default Display Text Format:  
_{Name:T} #{Code}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.MeasurementCategories](General.MeasurementCategories.md)  
Aggregate Root:  
[General.MeasurementCategories](General.MeasurementCategories.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.MeasurementUnits.md#code) | string (16) __nullable__ | When not null, contains unique measurement unit code. `Filter(eq;like)` `ORD` 
| [Description](General.MeasurementUnits.md#description) | [MultilanguageString](../data-types.md#multilanguagestring) __nullable__ | Full multi-language description of the measurement unit. 
| [Divisor](General.MeasurementUnits.md#divisor) | decimal (9, 3) | Divisor of the relative value of the measurement unit against other units (divisor when converting to base). `Required` `Default(1)` 
| [Id](General.MeasurementUnits.md#id) | guid |  
| [IsDefaultUnit](General.MeasurementUnits.md#isdefaultunit) | boolean | True if this measurement unit is the default measurement unit within the category. There can be only one default measurement unit within a category. `Required` `Default(false)` `Filter(eq)` 
| [Multiplier](General.MeasurementUnits.md#multiplier) | decimal (9, 3) | Multiplier of the relative value of the measurement unit against other units (multiplier when converting to base). `Required` `Default(1)` 
| [Name](General.MeasurementUnits.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the measurement unit. `Required` `Filter(eq;like)` `ORD` 
| [SystemUnit](General.MeasurementUnits.md#systemunit) | [SystemUnit](General.MeasurementUnits.md#systemunit) __nullable__ | Not null only when this is one of the system measurement units. N=NetKG; G=GrossKG; V=VolumeL; H=HeightM; W=WidthM, L=LengthM, P=Piece, T=TimeH. `Filter(eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MeasurementCategory](General.MeasurementUnits.md#measurementcategory) | [MeasurementCategories](General.MeasurementCategories.md) | Base measurement category Id. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Code

When not null, contains unique measurement unit code. `Filter(eq;like)` `ORD`

_Type_: **string (16) __nullable__**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **16**  

### Description

Full multi-language description of the measurement unit.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Divisor

Divisor of the relative value of the measurement unit against other units (divisor when converting to base). `Required` `Default(1)`

_Type_: **decimal (9, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDefaultUnit

True if this measurement unit is the default measurement unit within the category. There can be only one default measurement unit within a category. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Multiplier

Multiplier of the relative value of the measurement unit against other units (multiplier when converting to base). `Required` `Default(1)`

_Type_: **decimal (9, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### Name

Name of the measurement unit. `Required` `Filter(eq;like)` `ORD`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### SystemUnit

Not null only when this is one of the system measurement units. N=NetKG; G=GrossKG; V=VolumeL; H=HeightM; W=WidthM, L=LengthM, P=Piece, T=TimeH. `Filter(eq;like)`

_Type_: **[SystemUnit](General.MeasurementUnits.md#systemunit) __nullable__**  
Allowed values for the `SystemUnit`(General.MeasurementUnits.md#systemunit) data attribute  
_Allowed Values (General.MeasurementUnitsRepository.SystemUnit Enum Members)_  

| Value | Description |
| ---- | --- |
| GrossKilograms | GrossKilograms value. Stored as 'G'. <br /> _Database Value:_ 'G' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'GrossKilograms' |
| HeightMeters | HeightMeters value. Stored as 'H'. <br /> _Database Value:_ 'H' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'HeightMeters' |
| LengthMeters | LengthMeters value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'LengthMeters' |
| NetKilograms | NetKilograms value. Stored as 'N'. <br /> _Database Value:_ 'N' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'NetKilograms' |
| Pieces | Pieces value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Pieces' |
| VolumeLiters | VolumeLiters value. Stored as 'V'. <br /> _Database Value:_ 'V' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'VolumeLiters' |
| WidthMeters | WidthMeters value. Stored as 'W'. <br /> _Database Value:_ 'W' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'WidthMeters' |
| TimeHours | TimeHours value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'TimeHours' |

_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### MeasurementCategory

Base measurement category Id. `Required` `Filter(multi eq)` `Owner`

_Type_: **[MeasurementCategories](General.MeasurementCategories.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=General.MeasurementUnits erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.MeasurementUnits erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_MeasurementUnits?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_MeasurementUnits?$top=10>

