---
uid: Crm.Sales.DocumentTypePaymentOptions
---
# Crm.Sales.DocumentTypePaymentOptions

Contains payment options for user documnet types for sales orders. Entity: Crm_Document_Type_Payment_Options

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Sales.DocumentTypePaymentOptions.md#Id) | guid |  
| [DeferredPaymentMinimalAmmount](Crm.Sales.DocumentTypePaymentOptions.md#DeferredPaymentMinimalAmmount) | [Amount](../data-types.md#Amount) | The minimal order total amount, which an order must have in order to use deferred payment. [Currency: DeferredPaymentMinimalAmmountCurrency] [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DeferredPaymentMinimalAmmountCurrency](Crm.Sales.DocumentTypePaymentOptions.md#DeferredPaymentMinimalAmmountCurrency) | [General.Currencies](General.Currencies.md) | The currency of Deferred Payment Minimal Amount. [Required] [Filter(multi eq)] |
| [DocumentType](Crm.Sales.DocumentTypePaymentOptions.md#DocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The document type for which the payment option applies. [Required] [Filter(multi eq)] |
| [EnterpriseCompany](Crm.Sales.DocumentTypePaymentOptions.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company for which the payment options are specified. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DeferredPaymentMinimalAmmount

> The minimal order total amount, which an order must have in order to use deferred payment. [Currency: DeferredPaymentMinimalAmmountCurrency] [Required]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### DeferredPaymentMinimalAmmountCurrency

> The currency of Deferred Payment Minimal Amount. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DocumentType

> The document type for which the payment option applies. [Required] [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> The enterprise company for which the payment options are specified. [Required] [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Sales.DocumentTypePaymentOptions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Sales.DocumentTypePaymentOptions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Sales.DocumentTypePaymentOptions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_DocumentTypePaymentOptions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_DocumentTypePaymentOptions?$top=10>

