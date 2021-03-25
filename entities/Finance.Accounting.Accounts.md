---
uid: Finance.Accounting.Accounts
---
# Finance.Accounting.Accounts Entity

**Namespace:** [Finance.Accounting](Finance.Accounting.md)  

Contains the leaf level of the chart of accounts. Entity: Acc_Accounts

## Default Visualization
Default Display Text Format:  
_{AccountFullNumber}: {Name:T}_  
Default Search Member:  
_AccountFullNumber_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Accounting.Accounts](Finance.Accounting.Accounts.md)  
  * [Finance.Accounting.AccountRequiredProperties](Finance.Accounting.AccountRequiredProperties.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AccountFullNumber](Finance.Accounting.Accounts.md#accountfullnumber) | string(30) | The full number of the account, unique among all accounts. It consists of the group number, concatenated with the account number. `Required` `Filter(like)` `ReadOnly` 
| [CurrencyValuationMethod](Finance.Accounting.Accounts.md#currencyvaluationmethod) | [CurrencyValuationMethod](Finance.Accounting.Accounts.md#currencyvaluationmethod) | Method for base currency valuation of non base currency amounts. ACB = Account_Current_Balance, DCD = Document_Currency_<br />Directory, BRD=Balance_Reference_<br />Document. `Required` `Default("ACB")` 
| [Description](Finance.Accounting.Accounts.md#description) | string(254) (nullable) | The description of this Account. 
| [Discontinued](Finance.Accounting.Accounts.md#discontinued) | boolean | True means that the account won't be used any more and should not appear in combo boxes. `Required` `Default(false)` `Filter(eq)` 
| [Id](Finance.Accounting.Accounts.md#id) | guid |  
| [Name](Finance.Accounting.Accounts.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The account name. `Required` `Filter(like)` 
| [Number](Finance.Accounting.Accounts.md#number) | string(30) | The number of the account, unique within the account group. `Required` `Filter(like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccountGroup](Finance.Accounting.Accounts.md#accountgroup) | [AccountGroups](Finance.Accounting.AccountGroups.md) | The account group to which this account belongs. `Required` `Filter(multi eq)` |
| [Currency](Finance.Accounting.Accounts.md#currency) | [Currencies](General.Currencies.md) (nullable) | The primary currency of the account. All movements on the account are stored in this currency. If there are movements on the account, the currency cannot be changed. `Filter(multi eq)` |
| [EnterpriseCompany](Finance.Accounting.Accounts.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this Account applies, or null if it is for all enterprise companies. `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| RequiredProperties | [AccountRequiredProperties](Finance.Accounting.AccountRequiredProperties.md) | List of `AccountRequiredProperty`(Finance.Accounting.AccountRequiredProperties.md) child objects, based on the `Finance.Accounting.AccountRequiredProperty.Account`(Finance.Accounting.AccountRequiredProperties.md#account) back reference 


## Attribute Details

### AccountFullNumber

The full number of the account, unique among all accounts. It consists of the group number, concatenated with the account number. `Required` `Filter(like)` `ReadOnly`

_Type_: **string(30)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **30**  

### CurrencyValuationMethod

Method for base currency valuation of non base currency amounts. ACB = Account_Current_Balance, DCD = Document_Currency_Directory, BRD=Balance_Reference_Document. `Required` `Default("ACB")`

_Type_: **[CurrencyValuationMethod](Finance.Accounting.Accounts.md#currencyvaluationmethod)**  
Allowed values for the `CurrencyValuationMethod`(Finance.Accounting.Accounts.md#currencyvaluationmethod) data attribute  
_Allowed Values (Finance.Accounting.AccountsRepository.CurrencyValuationMethod Enum Members)_  

| Value | Description |
| ---- | --- |
| AccountCurrentBalance | AccountCurrentBalance value. Stored as 'ACB'. <br /> _Database Value:_ 'ACB' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AccountCurrentBalance' |
| DocumentCurrencyDirectory | DocumentCurrencyDirectory value. Stored as 'DCD'. <br /> _Database Value:_ 'DCD' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'DocumentCurrencyDirectory' |
| BalanceReferenceDocument | BalanceReferenceDocument value. Stored as 'BRD'. <br /> _Database Value:_ 'BRD' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'BalanceReferenceDocument' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **AccountCurrentBalance**  

### Description

The description of this Account.

_Type_: **string(254) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Discontinued

True means that the account won't be used any more and should not appear in combo boxes. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The account name. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Number

The number of the account, unique within the account group. `Required` `Filter(like)`

_Type_: **string(30)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **30**  


## Reference Details

### AccountGroup

The account group to which this account belongs. `Required` `Filter(multi eq)`

_Type_: **[AccountGroups](Finance.Accounting.AccountGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Currency

The primary currency of the account. All movements on the account are stored in this currency. If there are movements on the account, the currency cannot be changed. `Filter(multi eq)`

_Type_: **[Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

The Enterprise Company to which this Account applies, or null if it is for all enterprise companies. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Accounting.Accounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Accounting.Accounts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_Accounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_Accounts?$top=10>

