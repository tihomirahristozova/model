---
uid: Applications.Rental.TransactionLines
---
# Applications.Rental.TransactionLines Entity

**Namespace:** [Applications.Rental](Applications.Rental.md)  

Contains all transactions of Record of Handover / Handing-Over Record lines. Entity: Rent_Transaction_Lines

## Default Visualization
Default Display Text Format:  
_{RentTransaction.EntityName}_  
Default Search Members:  
_RentTransaction.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Rental.Transactions](Applications.Rental.Transactions.md)  
Aggregate Root:  
[Applications.Rental.Transactions](Applications.Rental.Transactions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Rental.TransactionLines.md#id) | guid |  
| [Notes](Applications.Rental.TransactionLines.md#notes) | string (max) __nullable__ | Notes. 
| [ObjectVersion](Applications.Rental.TransactionLines.md#objectversion) | int32 |  
| [TransactionTimestamp](Applications.Rental.TransactionLines.md#transactiontimestamp) | datetime | Transaction Timestamp. `Required` `Filter(multi eq;ge;le)` 
| [TransactionType](Applications.Rental.TransactionLines.md#transactiontype) | [TransactionType](Applications.Rental.TransactionLines.md#transactiontype) | Transaction Type. `Required` `Filter(eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [LeaseContract](Applications.Rental.TransactionLines.md#leasecontract) | [LeaseContracts](Applications.Rental.LeaseContracts.md) | Lease Contract. `Required` `Filter(multi eq)` |
| [LesseeCustomer](Applications.Rental.TransactionLines.md#lesseecustomer) | [Customers](Crm.Customers.md) | Lessee Customer. `Required` `Filter(multi eq)` |
| [RentalAsset](Applications.Rental.TransactionLines.md#rentalasset) | [Assets](Applications.Rental.Assets.md) | Rental asset. `Required` `Filter(multi eq)` |
| [RentTransaction](Applications.Rental.TransactionLines.md#renttransaction) | [Transactions](Applications.Rental.Transactions.md) | The <see cref="Transaction"/> to which this TransactionLine belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### TransactionTimestamp

Transaction Timestamp. `Required` `Filter(multi eq;ge;le)`

_Type_: **datetime**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

### TransactionType

Transaction Type. `Required` `Filter(eq;like)`

_Type_: **[TransactionType](Applications.Rental.TransactionLines.md#transactiontype)**  
Allowed values for the `TransactionType`(Applications.Rental.TransactionLines.md#transactiontype) data attribute  
_Allowed Values (Applications.Rental.TransactionLinesRepository.TransactionType Enum Members)_  

| Value | Description |
| ---- | --- |
| Deliver | Deliver value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Deliver' |
| Receive | Receive value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Receive' |
| WriteOffNotReturned | WriteOffNotReturned value. Stored as 'W'. <br /> _Database Value:_ 'W' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'WriteOffNotReturned' |
| StatusReport | StatusReport value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'StatusReport' |

_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### LeaseContract

Lease Contract. `Required` `Filter(multi eq)`

_Type_: **[LeaseContracts](Applications.Rental.LeaseContracts.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### LesseeCustomer

Lessee Customer. `Required` `Filter(multi eq)`

_Type_: **[Customers](Crm.Customers.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### RentalAsset

Rental asset. `Required` `Filter(multi eq)`

_Type_: **[Assets](Applications.Rental.Assets.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### RentTransaction

The <see cref="Transaction"/> to which this TransactionLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Transactions](Applications.Rental.Transactions.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Applications.Rental.TransactionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Rental.TransactionLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_TransactionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_TransactionLines?$top=10>

