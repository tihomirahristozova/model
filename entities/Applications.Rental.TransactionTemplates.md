---
uid: Applications.Rental.TransactionTemplates
---
# Applications.Rental.TransactionTemplates

Specifies additional options for document routes, generating Rental Transactions. Entity: Rent_Transaction_Templates

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Rental.TransactionTemplates.md#id) | guid |  
| [TransactionType](Applications.Rental.TransactionTemplates.md#transactiontype) | [TransactionType](Applications.Rental.TransactionTemplates.md#transactiontype) | Transaction type for the rent transaction that is to be created. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Route](Applications.Rental.TransactionTemplates.md#route) | [Routes](Systems.Workflow.Routes.md) | The route for which the transaction template is defined. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### TransactionType

> Transaction type for the rent transaction that is to be created. [Required]

_Type_: **[TransactionType](Applications.Rental.TransactionTemplates.md#transactiontype)**  
Allowed values for the [TransactionType](Applications.Rental.Transactions.md#transactiontype) data attribute  
_Allowed Values (Applications.Rental.TransactionsRepository.TransactionType Enum Members)_  

| Value | Description |
| ---- | --- |
| Deliver | Deliver value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Deliver' |
| Receive | Receive value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Receive' |
| WriteOffNotReturned | WriteOffNotReturned value. Stored as 'W'. <br /> _Database Value:_ 'W' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'WriteOffNotReturned' |
| StatusReport | StatusReport value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'StatusReport' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Route

> The route for which the transaction template is defined. [Required] [Filter(multi eq)]

_Type_: **[Routes](Systems.Workflow.Routes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Rental.TransactionTemplates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Rental.TransactionTemplates erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Rental.TransactionTemplates erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_TransactionTemplates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_TransactionTemplates?$top=10>

