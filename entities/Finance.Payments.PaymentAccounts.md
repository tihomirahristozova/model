---
uid: Finance.Payments.PaymentAccounts
---
# Finance.Payments.PaymentAccounts

Payment accounts are cash, bank and other accounts, which are used in payments. Payment accounts are frequently used as analytical dimensions (properties) for general ledger accounts. Entity: Cash_Payment_Accounts

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Payments.PaymentAccounts.md#code) | string | The unique code of the PaymentAccount. [Required] [Filter(eq;like)] [ORD] 
| [Id](Finance.Payments.PaymentAccounts.md#id) | guid |  
| [IsActive](Finance.Payments.PaymentAccounts.md#isactive) | boolean | Indicates wheather the payment account is currently used (active). [Required] [Default(true)] [Filter(eq)] 
| [Name](Finance.Payments.PaymentAccounts.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this PaymentAccount. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Finance.Payments.PaymentAccounts.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this PaymentAccount. Null means that all users have unlimited permissions. [Filter(multi eq)] |
| [BankAccount](Finance.Payments.PaymentAccounts.md#bankaccount) | [PartyBankAccounts](General.Contacts.PartyBankAccounts.md) (nullable) | The bank account, which is represented by this payment account. [Filter(multi eq)] |
| [Currency](Finance.Payments.PaymentAccounts.md#currency) | [Currencies](General.Currencies.md) | The currency in which the movements for this payment account will be recorded. [Required] [Filter(multi eq)] |
| [EnterpriseCompany](Finance.Payments.PaymentAccounts.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this PaymentAccount applies, or null if it is for all enterprise companies. [Filter(multi eq)] |
| [EnterpriseCompanyLocation](Finance.Payments.PaymentAccounts.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The Enterprise Company Location to which this PaymentAccount applies, or null if it is for all enterprise company locations. [Filter(multi eq)] |
| [PaymentType](Finance.Payments.PaymentAccounts.md#paymenttype) | [PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | Specifies the payment type used to pay, when using this payment account. null when the payment type is unknown or unspecified. [Filter(multi eq)] |


## Attribute Details

### Code

> The unique code of the PaymentAccount. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

> Indicates wheather the payment account is currently used (active). [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

> The name of this PaymentAccount. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

> The access key, containing the user permissions for this PaymentAccount. Null means that all users have unlimited permissions. [Filter(multi eq)]

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### BankAccount

> The bank account, which is represented by this payment account. [Filter(multi eq)]

_Type_: **[PartyBankAccounts](General.Contacts.PartyBankAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Currency

> The currency in which the movements for this payment account will be recorded. [Required] [Filter(multi eq)]

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

> The Enterprise Company to which this PaymentAccount applies, or null if it is for all enterprise companies. [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

> The Enterprise Company Location to which this PaymentAccount applies, or null if it is for all enterprise company locations. [Filter(multi eq)]

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PaymentType

> Specifies the payment type used to pay, when using this payment account. null when the payment type is unknown or unspecified. [Filter(multi eq)]

_Type_: **[PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Payments.PaymentAccounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Payments.PaymentAccounts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Payments.PaymentAccounts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_PaymentAccounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_PaymentAccounts?$top=10>

