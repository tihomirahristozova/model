---
uid: Logistics.LogisticUnitContents
---
# Logistics.LogisticUnitContents Entity

**Namespace:** [Logistics](Logistics.md)  

Theoretical or actual content of a logistic unit. Entity: Log_Logistic_Unit_Contents (Introduced in version 21.1.0.77)

## Default Visualization
Default Display Text Format:  
_{LogisticUnit}_  
Default Search Members:  
_LotNumber; LogisticUnit_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.LogisticUnits](Logistics.LogisticUnits.md)  
Aggregate Root:  
[Logistics.LogisticUnits](Logistics.LogisticUnits.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BaseQuantity](Logistics.LogisticUnitContents.md#basequantity) | decimal (12, 3) | The quantity, expressed in the base measurement category of the product. `Required` `Filter(eq;ge;le)` 
| [ExpirationDate](Logistics.LogisticUnitContents.md#expirationdate) | date __nullable__ | Expiration date of the goods. null means unknown or N/A. `Filter(multi eq;ge;le)` 
| [GrossWeight](Logistics.LogisticUnitContents.md#grossweight) | decimal (12, 3) __nullable__ | Gross weight in kilograms (kg). null means unknown. `Filter(eq;ge;le)` 
| [Id](Logistics.LogisticUnitContents.md#id) | guid |  
| [LineNo](Logistics.LogisticUnitContents.md#lineno) | int32 | Consecutive position within the logistic unit. `Required` `Filter(multi eq)` 
| [LotNumber](Logistics.LogisticUnitContents.md#lotnumber) | string (32) __nullable__ | The production lot number. null means unknown. `Filter(multi eq;like)` 
| [Notes](Logistics.LogisticUnitContents.md#notes) | string (max) __nullable__ | Notes for this LogisticUnitContent. 
| [Quantity](Logistics.LogisticUnitContents.md#quantity) | decimal (12, 3) | Quantity of the product in the logistic unit. Expressed in the specified measurement unit. `Required` `Filter(multi eq;ge;le)` 
| [StandardQuantity](Logistics.LogisticUnitContents.md#standardquantity) | decimal (12, 3) | The quantity, expessed in the standard measurement unit of the product. `Required` `Filter(eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [LogisticUnit](Logistics.LogisticUnitContents.md#logisticunit) | [LogisticUnits](Logistics.LogisticUnits.md) | The containing logistic unit. `Required` `Filter(multi eq)` `Owner` |
| [Product](Logistics.LogisticUnitContents.md#product) | [Products](General.Products.Products.md) | The product, which is contained in the logistic unit. `Required` `Filter(multi eq)` |
| [QuantityUnit](Logistics.LogisticUnitContents.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of the quantity. `Required` `Filter(multi eq)` |


## Attribute Details

### BaseQuantity

The quantity, expressed in the base measurement category of the product. `Required` `Filter(eq;ge;le)`

_Type_: **decimal (12, 3)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ExpirationDate

Expiration date of the goods. null means unknown or N/A. `Filter(multi eq;ge;le)`

_Type_: **date __nullable__**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

### GrossWeight

Gross weight in kilograms (kg). null means unknown. `Filter(eq;ge;le)`

_Type_: **decimal (12, 3) __nullable__**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive position within the logistic unit. `Required` `Filter(multi eq)`

_Type_: **int32**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.LogisticUnit.Contents.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.LogisticUnit.Contents.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### LotNumber

The production lot number. null means unknown. `Filter(multi eq;like)`

_Type_: **string (32) __nullable__**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### Notes

Notes for this LogisticUnitContent.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Quantity

Quantity of the product in the logistic unit. Expressed in the specified measurement unit. `Required` `Filter(multi eq;ge;le)`

_Type_: **decimal (12, 3)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

### StandardQuantity

The quantity, expessed in the standard measurement unit of the product. `Required` `Filter(eq;ge;le)`

_Type_: **decimal (12, 3)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### LogisticUnit

The containing logistic unit. `Required` `Filter(multi eq)` `Owner`

_Type_: **[LogisticUnits](Logistics.LogisticUnits.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Product

The product, which is contained in the logistic unit. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

The measurement unit of the quantity. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Logistics.LogisticUnitContents erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.LogisticUnitContents erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_LogisticUnitContents?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_LogisticUnitContents?$top=10>

