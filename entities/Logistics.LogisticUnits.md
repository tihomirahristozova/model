---
uid: Logistics.LogisticUnits
---
# Logistics.LogisticUnits Entity

**Namespace:** [Logistics](Logistics.md)  

Composition of products established for transport and/or storage which needs to be managed through the supply chain. Entity: Log_Logistic_Units (Introduced in version 21.1.0.77)

## Default Visualization
Default Display Text Format:  
_{SerialCode}_  
Default Search Member:  
_SerialCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.LogisticUnits](Logistics.LogisticUnits.md)  
  * [Logistics.LogisticUnitContents](Logistics.LogisticUnitContents.md)  
  * [Logistics.LogisticUnitSpecifications](Logistics.LogisticUnitSpecifications.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ExpectedWeight](Logistics.LogisticUnits.md#expectedweight) | decimal(12, 3) (nullable) | Expected weight in KG. Used for planning purposes. null means unknown. `Filter(eq;ge;le)` 
| [Id](Logistics.LogisticUnits.md#id) | guid |  
| [MeasuredWeight](Logistics.LogisticUnits.md#measuredweight) | decimal(12, 3) (nullable) | Actual measured weight of the unit in KG. null means unknown. `Filter(eq;ge;le)` 
| [Notes](Logistics.LogisticUnits.md#notes) | string(2147483647) (nullable) | Notes for this LogisticUnit. `Filter(like)` 
| [SerialCode](Logistics.LogisticUnits.md#serialcode) | string(32) | Unique serial code of the logistic unit. If GS1 coding is used, this is the SSCC. `Required` `Filter(multi eq;like)` `ORD` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CargoType](Logistics.LogisticUnits.md#cargotype) | [CargoTypes](Logistics.Shipment.CargoTypes.md) (nullable) | General type of the cargo of the logistic unit. null means unknown or N/A. `Filter(multi eq)` |
| [LogisticUnitType](Logistics.LogisticUnits.md#logisticunittype) | [LogisticUnitTypes](Logistics.LogisticUnitTypes.md) (nullable) | The type of the logistic unit. null means the type is currently unknown. `Filter(multi eq)` |
| [RepresentedAsProduct](Logistics.LogisticUnits.md#representedasproduct) | [Products](General.Products.Products.md) (nullable) | When the logistic unit is also a tradeable item, specifies the product used to trade the unit. The product should uniquely identify only one logistic unit. Note that this is different from a logistic unit containing a single item. null means that the unit is not a tradeable item. `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Contents | [LogisticUnitContents](Logistics.LogisticUnitContents.md) | List of `LogisticUnitContent`(Logistics.LogisticUnitContents.md) child objects, based on the `Logistics.LogisticUnitContent.LogisticUnit`(Logistics.LogisticUnitContents.md#logisticunit) back reference 
| Specifications | [LogisticUnitSpecifications](Logistics.LogisticUnitSpecifications.md) | List of `LogisticUnitSpecification<br />`(Logistics.LogisticUnitSpecifications.md) child objects, based on the `Logistics.LogisticUnitSpecification.LogisticUnit`(Logistics.LogisticUnitSpecifications.md#logisticunit) back reference 


## Attribute Details

### ExpectedWeight

Expected weight in KG. Used for planning purposes. null means unknown. `Filter(eq;ge;le)`

_Type_: **decimal(12, 3) (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### MeasuredWeight

Actual measured weight of the unit in KG. null means unknown. `Filter(eq;ge;le)`

_Type_: **decimal(12, 3) (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Notes

Notes for this LogisticUnit. `Filter(like)`

_Type_: **string(2147483647) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### SerialCode

Unique serial code of the logistic unit. If GS1 coding is used, this is the SSCC. `Required` `Filter(multi eq;like)` `ORD`

_Type_: **string(32)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  
_Maximum Length_: **32**  


## Reference Details

### CargoType

General type of the cargo of the logistic unit. null means unknown or N/A. `Filter(multi eq)`

_Type_: **[CargoTypes](Logistics.Shipment.CargoTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### LogisticUnitType

The type of the logistic unit. null means the type is currently unknown. `Filter(multi eq)`

_Type_: **[LogisticUnitTypes](Logistics.LogisticUnitTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### RepresentedAsProduct

When the logistic unit is also a tradeable item, specifies the product used to trade the unit. The product should uniquely identify only one logistic unit. Note that this is different from a logistic unit containing a single item. null means that the unit is not a tradeable item. `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### UpdateGS1ApplicationCodes

Based on the internal data in the logistic unit and its contents, creates or updates the GS1 application codes.              The data is than stored in the logistic unit specifications.              The method does not commit the object transaction.  
_Return Type_: **void**  
_Declaring Type_: **[LogisticUnits](Logistics.LogisticUnits.md)**  
_Domain API Request_: **POST**  


## Business Rules

[!list erp.entity=Logistics.LogisticUnits erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.LogisticUnits erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_LogisticUnits?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_LogisticUnits?$top=10>

