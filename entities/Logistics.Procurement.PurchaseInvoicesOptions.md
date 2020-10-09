---
uid: Logistics.Procurement.PurchaseInvoicesOptions
---
# Logistics.Procurement.PurchaseInvoicesOptions Entity

Contains purchase invoice specific options for the different document types. Entity: Scm_Purchase_Invoices_Options

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Procurement.PurchaseInvoicesOptions.md#id) | guid |  
| [SignRestriction](Logistics.Procurement.PurchaseInvoicesOptions.md#signrestriction) | [SignRestriction](Logistics.Procurement.PurchaseInvoicesOptions.md#signrestriction) | This option can restrict the sign of the Line Amounts for each detail line in purchase invoices of the specified document type. [Required] [Default(0)] 
| [TotalAmountSignRestriction](Logistics.Procurement.PurchaseInvoicesOptions.md#totalamountsignrestriction) | [TotalAmountSignRestriction](Logistics.Procurement.PurchaseInvoicesOptions.md#totalamountsignrestriction) | This option can restrict the sign of the Total Amounts of the purchase invoices of the specified document type. The restriction is applied upon document Release. [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](Logistics.Procurement.PurchaseInvoicesOptions.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type, for which the options are specified. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### SignRestriction

> This option can restrict the sign of the Line Amounts for each detail line in purchase invoices of the specified document type. [Required] [Default(0)]

_Type_: **[SignRestriction](Logistics.Procurement.PurchaseInvoicesOptions.md#signrestriction)**  
Allowed values for the [SignRestriction](Logistics.Procurement.PurchaseInvoicesOptions.md#signrestriction) data attribute  
_Allowed Values (Logistics.Procurement.PurchaseInvoicesOptionsRepository.SignRestriction Enum Members)_  

| Value | Description |
| ---- | --- |
| AllowAll | AllowAll value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AllowAll' |
| AllowOnlyPositive | AllowOnlyPositive value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'AllowOnlyPositive' |
| AllowOnlyNegative | AllowOnlyNegative value. Stored as -1. <br /> _Database Value:_ -1 <br /> _Model Value:_ -1 <br /> _Domain API Value:_ 'AllowOnlyNegative' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### TotalAmountSignRestriction

> This option can restrict the sign of the Total Amounts of the purchase invoices of the specified document type. The restriction is applied upon document Release. [Required] [Default(0)]

_Type_: **[TotalAmountSignRestriction](Logistics.Procurement.PurchaseInvoicesOptions.md#totalamountsignrestriction)**  
Allowed values for the [TotalAmountSignRestriction](Logistics.Procurement.PurchaseInvoicesOptions.md#totalamountsignrestriction) data attribute  
_Allowed Values (Logistics.Procurement.PurchaseInvoicesOptionsRepository.TotalAmountSignRestriction Enum Members)_  

| Value | Description |
| ---- | --- |
| AllowAll | AllowAll value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AllowAll' |
| AllowOnlyPositive | AllowOnlyPositive value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'AllowOnlyPositive' |
| AllowOnlyNegative | AllowOnlyNegative value. Stored as -1. <br /> _Database Value:_ -1 <br /> _Model Value:_ -1 <br /> _Domain API Value:_ 'AllowOnlyNegative' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### DocumentType

> The document type, for which the options are specified. [Required] [Filter(multi eq)]

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseInvoicesOptions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseInvoicesOptions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Procurement.PurchaseInvoicesOptions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_PurchaseInvoicesOptions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_PurchaseInvoicesOptions?$top=10>

