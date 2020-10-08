---
uid: Applications.Rental.LeaseContractLineConsumables
---
# Applications.Rental.LeaseContractLineConsumables

Contains the consumables, which are sold accompanying asset rentals. Entity: Rent_Lease_Contract_Line_Consumables

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Rental.LeaseContractLineConsumables.md#Id) | guid |  
| [ConsumableQuantity](Applications.Rental.LeaseContractLineConsumables.md#ConsumableQuantity) | [Quantity](../data-types.md#Quantity) | The quantity sold of the consumable. [Unit: ConsumableQuantityUnit] [Required] [Default(0)] 
| [LineNo](Applications.Rental.LeaseContractLineConsumables.md#LineNo) | int32 | Consecutive number of the consumable within the lease contract line. [Required] [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ConsumableQuantityUnit](Applications.Rental.LeaseContractLineConsumables.md#ConsumableQuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Consumable Quantity. [Required] [Filter(multi eq)] |
| [LeaseLine](Applications.Rental.LeaseContractLineConsumables.md#LeaseLine) | [Applications.Rental.LeaseContractLines](Applications.Rental.LeaseContractLines.md) | Lease line with which the current consumable is given. [Required] [Filter(multi eq)] [Owner] |
| [Product](Applications.Rental.LeaseContractLineConsumables.md#Product) | [General.Products.Products](General.Products.Products.md) | The consumable to be sold accompanying the asset. [Required] [Filter(multi eq)] |
| [Store](Applications.Rental.LeaseContractLineConsumables.md#Store) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) | Store from which the consumable is issued. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ConsumableQuantity

> The quantity sold of the consumable. [Unit: ConsumableQuantityUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### LineNo

> Consecutive number of the consumable within the lease contract line. [Required] [Filter(eq;ge;le)]

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.LeaseLine.Consumables.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.LeaseLine.Consumables.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

## Reference Details

### ConsumableQuantityUnit

> The measurement unit of Consumable Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### LeaseLine

> Lease line with which the current consumable is given. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Rental.LeaseContractLines](Applications.Rental.LeaseContractLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The consumable to be sold accompanying the asset. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Store

> Store from which the consumable is issued. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Rental.LeaseContractLineConsumables erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Rental.LeaseContractLineConsumables erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Rental.LeaseContractLineConsumables erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_LeaseContractLineConsumables?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_LeaseContractLineConsumables?$top=10>

