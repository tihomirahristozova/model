---
uid: Applications.Rental.LeaseContractLines
---
# Applications.Rental.LeaseContractLines Entity

**Namespace:** [Applications.Rental](Applications.Rental.md)  

The detail lines of rental contracts. Each line contains rental conditions for one asset of the rental contract. Entity: Rent_Lease_Contract_Lines

## Default Visualization
Default Display Text Format:  
_{LeaseContract.DocumentType.Code}:{LeaseContract.DocumentNo} - {LeaseContract.DocumentType.TypeName:T}_  
Default Search Member:  
_LeaseContract.DocumentType.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Rental.LeaseContracts](Applications.Rental.LeaseContracts.md)  
Aggregate Root:  
[Applications.Rental.LeaseContracts](Applications.Rental.LeaseContracts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EndDate](Applications.Rental.LeaseContractLines.md#enddate) | date | Ending date of lease of this asset. `Required` `Filter(multi eq;ge;le)` 
| [GuaranteeAmount](Applications.Rental.LeaseContractLines.md#guaranteeamount) | [Amount](../data-types.md#amount) (nullable) | Deposit amount in the currency of the document which is given for this asset during its period of lease. `Currency: LeaseContract.Currency` 
| [Id](Applications.Rental.LeaseContractLines.md#id) | guid |  
| [LineNo](Applications.Rental.LeaseContractLines.md#lineno) | int32 | Consecutive number of the line within the lease contract. `Required` `Filter(eq;ge;le)` 
| [LineNotes](Applications.Rental.LeaseContractLines.md#linenotes) | string(2147483647) (nullable) | Notes for this line. 
| [StartDate](Applications.Rental.LeaseContractLines.md#startdate) | date | Starting date of lease for this asset. `Required` `Filter(multi eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [LeaseContract](Applications.Rental.LeaseContractLines.md#leasecontract) | [LeaseContracts](Applications.Rental.LeaseContracts.md) | The `LeaseContract`(Applications.Rental.LeaseContractLines.md#leasecontract) to which this LeaseContractLine belongs. `Required` `Filter(multi eq)` `Owner` |
| [RentalAsset](Applications.Rental.LeaseContractLines.md#rentalasset) | [Assets](Applications.Rental.Assets.md) | The asset which is rented with the current contract. `Required` `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Consumables | [LeaseContractLineConsumables](Applications.Rental.LeaseContractLineConsumables.md) | List of `LeaseContract<br />LineConsumable`(Applications.Rental.LeaseContractLine<br />Consumables.md) child objects, based on the `Applications.Rental.LeaseContractLine<br />Consumable.LeaseLine`(Applications.Rental.LeaseContractLine<br />Consumables.md#leaseline) back reference 


## Attribute Details

### EndDate

Ending date of lease of this asset. `Required` `Filter(multi eq;ge;le)`

_Type_: **date**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.LeaseContract.EndDate`

_Front-End Recalc Expressions:_  
`obj.LeaseContract.EndDate`
### GuaranteeAmount

Deposit amount in the currency of the document which is given for this asset during its period of lease. `Currency: LeaseContract.Currency`

_Type_: **[Amount](../data-types.md#amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive number of the line within the lease contract. `Required` `Filter(eq;ge;le)`

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.LeaseContract.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.LeaseContract.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### LineNotes

Notes for this line.

_Type_: **string(2147483647) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### StartDate

Starting date of lease for this asset. `Required` `Filter(multi eq;ge;le)`

_Type_: **date**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.LeaseContract.StartDate`

_Front-End Recalc Expressions:_  
`obj.LeaseContract.StartDate`

## Reference Details

### LeaseContract

The `LeaseContract`(Applications.Rental.LeaseContractLines.md#leasecontract) to which this LeaseContractLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[LeaseContracts](Applications.Rental.LeaseContracts.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### RentalAsset

The asset which is rented with the current contract. `Required` `Filter(multi eq)`

_Type_: **[Assets](Applications.Rental.Assets.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Rental.LeaseContractLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Rental.LeaseContractLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_LeaseContractLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_LeaseContractLines?$top=10>

