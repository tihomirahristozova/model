---
uid: Applications.Rental.LeaseContractLineConsumables
---
# Applications.Rental.LeaseContractLineConsumables Entity

**Namespace:** [Applications.Rental](Applications.Rental.md)  

Contains the consumables, which are sold accompanying asset rentals. Entity: Rent_Lease_Contract_Line_Consumables

## Default Visualization
Default Display Text Format:  
_{LeaseLine.LeaseContract.EntityName}_  
Default Search Members:  
_LeaseLine.LeaseContract.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Rental.LeaseContractLines](Applications.Rental.LeaseContractLines.md)  
Aggregate Root:  
[Applications.Rental.LeaseContracts](Applications.Rental.LeaseContracts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ConsumableQuantity](Applications.Rental.LeaseContractLineConsumables.md#consumablequantity) | [Quantity (12, 3)](../data-types.md#quantity) | The quantity sold of the consumable. `Unit: ConsumableQuantityUnit` `Required` `Default(0)` 
| [Id](Applications.Rental.LeaseContractLineConsumables.md#id) | guid |  
| [LineNo](Applications.Rental.LeaseContractLineConsumables.md#lineno) | int32 | Consecutive number of the consumable within the lease contract line. `Required` `Filter(eq;ge;le)` 
| [ObjectVersion](Applications.Rental.LeaseContractLineConsumables.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ConsumableQuantityUnit](Applications.Rental.LeaseContractLineConsumables.md#consumablequantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Consumable Quantity. `Required` `Filter(multi eq)` |
| [LeaseLine](Applications.Rental.LeaseContractLineConsumables.md#leaseline) | [LeaseContractLines](Applications.Rental.LeaseContractLines.md) | Lease line with which the current consumable is given. `Required` `Filter(multi eq)` `Owner` |
| [Product](Applications.Rental.LeaseContractLineConsumables.md#product) | [Products](General.Products.Products.md) | The consumable to be sold accompanying the asset. `Required` `Filter(multi eq)` |
| [Store](Applications.Rental.LeaseContractLineConsumables.md#store) | [Stores](Logistics.Inventory.Stores.md) | Store from which the consumable is issued. `Required` `Filter(multi eq)` |


## Attribute Details

### ConsumableQuantity

The quantity sold of the consumable. `Unit: ConsumableQuantityUnit` `Required` `Default(0)`

_Type_: **[Quantity (12, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive number of the consumable within the lease contract line. `Required` `Filter(eq;ge;le)`

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.LeaseLine.Consumables.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.LeaseLine.Consumables.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### ConsumableQuantityUnit

The measurement unit of Consumable Quantity. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### LeaseLine

Lease line with which the current consumable is given. `Required` `Filter(multi eq)` `Owner`

_Type_: **[LeaseContractLines](Applications.Rental.LeaseContractLines.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Product

The consumable to be sold accompanying the asset. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

Store from which the consumable is issued. `Required` `Filter(multi eq)`

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Applications.Rental.LeaseContractLineConsumables erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Rental.LeaseContractLineConsumables erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_LeaseContractLineConsumables?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_LeaseContractLineConsumables?$top=10>

