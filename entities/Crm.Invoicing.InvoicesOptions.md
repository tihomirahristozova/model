---
uid: Crm.Invoicing.InvoicesOptions
---
# Crm.Invoicing.InvoicesOptions Entity

**Namespace:** [Crm.Invoicing](Crm.Invoicing.md)  

Default options for user document types for Invoices. Entity: Crm_Invoices_Options

## Default Visualization
Default Display Text Format:  
_{DocumentType.Code}: {DocumentType.EntityName:T}_  
Default Search Member:  
_DocumentType.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.DocumentTypes](General.DocumentTypes.md)  
Aggregate Root:  
[General.DocumentTypes](General.DocumentTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreatesVATEntries](Crm.Invoicing.InvoicesOptions.md#createsvatentries) | boolean | Specifies whether the invoices of the current type create entries in the VAT ledges. If is used, for instance, to determine if null VAT entry should be automatically created when the invoice is voided. `Required` `Default(true)` 
| [Id](Crm.Invoicing.InvoicesOptions.md#id) | guid |  
| [SignRestriction](Crm.Invoicing.InvoicesOptions.md#signrestriction) | [SignRestriction](Crm.Invoicing.InvoicesOptions.md#signrestriction) | Restricts the sign of the line amounts of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts. `Required` `Default(0)` 
| [TotalAmountSignRestriction](Crm.Invoicing.InvoicesOptions.md#totalamountsignrestriction) | [SignRestriction](Crm.Invoicing.InvoicesOptions.md#totalamountsignrestriction) | Restricts the sign of the total amount (amount to pay) of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts. `Required` `Default(0)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultDealType](Crm.Invoicing.InvoicesOptions.md#defaultdealtype) | [DealTypes](Finance.Vat.DealTypes.md) (nullable) | When not null, specifies default VAT deal type. `Filter(multi eq)` |
| [DocumentType](Crm.Invoicing.InvoicesOptions.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type for which the invoice option applies. `Required` `Filter(multi eq)` `Owner` |
| [VATDeviationDocument<br />AmountType](Crm.Invoicing.InvoicesOptions.md#vatdeviationdocumentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) (nullable) | Document amount that contains the difference between the total amount of the invoice formed by unit prices with VAT and the amount formed by unit prices without VAT. `Filter(multi eq)` |


## Attribute Details

### CreatesVATEntries

Specifies whether the invoices of the current type create entries in the VAT ledges. If is used, for instance, to determine if null VAT entry should be automatically created when the invoice is voided. `Required` `Default(true)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### SignRestriction

Restricts the sign of the line amounts of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts. `Required` `Default(0)`

_Type_: **[SignRestriction](Crm.Invoicing.InvoicesOptions.md#signrestriction)**  
Generic enum type for SignRestriction properties  
_Allowed Values (General.SignRestriction Enum Members)_  

| Value | Description |
| ---- | --- |
| AllowAll | AllowAll value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AllowAll' |
| AllowOnlyPositive | AllowOnlyPositive value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'AllowOnlyPositive' |
| AllowOnlyNegative | AllowOnlyNegative value. Stored as -1. <br /> _Database Value:_ -1 <br /> _Model Value:_ -1 <br /> _Domain API Value:_ 'AllowOnlyNegative' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### TotalAmountSignRestriction

Restricts the sign of the total amount (amount to pay) of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts. `Required` `Default(0)`

_Type_: **[SignRestriction](Crm.Invoicing.InvoicesOptions.md#totalamountsignrestriction)**  
Generic enum type for SignRestriction properties  
_Allowed Values (General.SignRestriction Enum Members)_  

| Value | Description |
| ---- | --- |
| AllowAll | AllowAll value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AllowAll' |
| AllowOnlyPositive | AllowOnlyPositive value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'AllowOnlyPositive' |
| AllowOnlyNegative | AllowOnlyNegative value. Stored as -1. <br /> _Database Value:_ -1 <br /> _Model Value:_ -1 <br /> _Domain API Value:_ 'AllowOnlyNegative' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### DefaultDealType

When not null, specifies default VAT deal type. `Filter(multi eq)`

_Type_: **[DealTypes](Finance.Vat.DealTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

The document type for which the invoice option applies. `Required` `Filter(multi eq)` `Owner`

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Can filter by attributes of referenced entity_: **True**  

### VATDeviationDocumentAmountType

Document amount that contains the difference between the total amount of the invoice formed by unit prices with VAT and the amount formed by unit prices without VAT. `Filter(multi eq)`

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Invoicing.InvoicesOptions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Invoicing.InvoicesOptions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Invoicing_InvoicesOptions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Invoicing_InvoicesOptions?$top=10>

