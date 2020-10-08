---
uid: Applications.Rental.LeaseContractLines
---
# Applications.Rental.LeaseContractLines

The detail lines of rental contracts. Each line contains rental conditions for one asset of the rental contract. Entity: Rent_Lease_Contract_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Rental.LeaseContractLines.md#Id) | guid |  
| [EndDate](Applications.Rental.LeaseContractLines.md#EndDate) | date | Ending date of lease of this asset. [Required] [Filter(multi eq;ge;le)] 
| [GuaranteeAmount](Applications.Rental.LeaseContractLines.md#GuaranteeAmount) | [Amount](../data-types.md#Amount) (nullable) | Deposit amount in the currency of the document which is given for this asset during its period of lease. [Currency: LeaseContract.Currency] 
| [LineNo](Applications.Rental.LeaseContractLines.md#LineNo) | int32 | Consecutive number of the line within the lease contract. [Required] [Filter(eq;ge;le)] 
| [LineNotes](Applications.Rental.LeaseContractLines.md#LineNotes) | string (nullable) | Notes for this line. 
| [StartDate](Applications.Rental.LeaseContractLines.md#StartDate) | date | Starting date of lease for this asset. [Required] [Filter(multi eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [LeaseContract](Applications.Rental.LeaseContractLines.md#LeaseContract) | [Applications.Rental.LeaseContracts](Applications.Rental.LeaseContracts.md) | The [LeaseContract](Applications.Rental.LeaseContractLines.md#LeaseContract) to which this LeaseContractLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [RentalAsset](Applications.Rental.LeaseContractLines.md#RentalAsset) | [Applications.Rental.Assets](Applications.Rental.Assets.md) | The asset which is rented with the current contract. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Consumables | [Applications.Rental.LeaseContractLineConsumables](Applications.Rental.LeaseContractLineConsumables.md) | List of [LeaseContractLineConsumable](Applications.Rental.LeaseContractLineConsumables.md) child objects, based on the [Applications.Rental.LeaseContractLineConsumable.LeaseLine](Applications.Rental.LeaseContractLineConsumables.md#LeaseLine) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### EndDate

> Ending date of lease of this asset. [Required] [Filter(multi eq;ge;le)]

_Type_: **date**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.LeaseContract.EndDate`

_Front-End Recalc Expressions:_  
`obj.LeaseContract.EndDate`
### GuaranteeAmount

> Deposit amount in the currency of the document which is given for this asset during its period of lease. [Currency: LeaseContract.Currency]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LineNo

> Consecutive number of the line within the lease contract. [Required] [Filter(eq;ge;le)]

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.LeaseContract.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.LeaseContract.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### LineNotes

> Notes for this line.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartDate

> Starting date of lease for this asset. [Required] [Filter(multi eq;ge;le)]

_Type_: **date**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.LeaseContract.StartDate`

_Front-End Recalc Expressions:_  
`obj.LeaseContract.StartDate`

## Reference Details

### LeaseContract

> The [LeaseContract](Applications.Rental.LeaseContractLines.md#LeaseContract) to which this LeaseContractLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Rental.LeaseContracts](Applications.Rental.LeaseContracts.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RentalAsset

> The asset which is rented with the current contract. [Required] [Filter(multi eq)]

_Type_: **[Applications.Rental.Assets](Applications.Rental.Assets.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Rental.LeaseContractLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Rental.LeaseContractLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Rental.LeaseContractLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_LeaseContractLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_LeaseContractLines?$top=10>

