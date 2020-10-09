---
uid: General.MeasurementCategories
---
# General.MeasurementCategories Entity

Categories of measurement units. The units within a category are directly convertable to each other. Each category contains one base unit and unlimited number of derived units with fixed ratio to the base unit. Entity: Gen_Measurement_Categories

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.MeasurementCategories.md#id) | guid |  
| [IsDefault](General.MeasurementCategories.md#isdefault) | boolean | True=This category is the default category; false=otherwise. [Required] [Default(false)] [Filter(eq)] 
| [Name](General.MeasurementCategories.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this MeasurementCategory. [Required] [Filter(eq;like)] [ORD] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| MeasurementUnits | [MeasurementUnits](General.MeasurementUnits.md) | List of [MeasurementUnit](General.MeasurementUnits.md) child objects, based on the [General.MeasurementUnit.MeasurementCategory](General.MeasurementUnits.md#measurementcategory) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDefault

True=This category is the default category; false=otherwise. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

The name of this MeasurementCategory. [Required] [Filter(eq;like)] [ORD]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  



## Business Rules

[!list erp.entity=General.MeasurementCategories erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.MeasurementCategories erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_MeasurementCategories?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_MeasurementCategories?$top=10>

