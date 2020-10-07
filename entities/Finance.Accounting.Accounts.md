# Finance.Accounting.Accounts

Contains the leaf level of the chart of accounts. Entity: Acc_Accounts

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Accounting.Accounts.md#Id) | guid |  
| [AccountFullNumber](Finance.Accounting.Accounts.md#AccountFullNumber) | string | The full number of the account, unique among all accounts. It consists of the group number, concatenated with the account number. [Required] [Filter(like)] [ReadOnly] 
| [Name](Finance.Accounting.Accounts.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | The account name. [Required] [Filter(like)] 
| [Number](Finance.Accounting.Accounts.md#Number) | string | The number of the account, unique within the account group. [Required] [Filter(like)] 
| [CurrencyValuationMethod](Finance.Accounting.Accounts.md#CurrencyValuationMethod) | [Finance.Accounting.AccountsRepository.CurrencyValuationMethod](Finance.Accounting.Accounts.md#CurrencyValuationMethod) | Method for base currency valuation of non base currency amounts. ACB = Account_Current_Balance, DCD = Document_Currency_Directory, BRD=Balance_Reference_Document. [Required] [Default("ACB")] 
| [Description](Finance.Accounting.Accounts.md#Description) | string (nullable) | The description of this Account. 
| [Discontinued](Finance.Accounting.Accounts.md#Discontinued) | boolean | True means that the account won't be used any more and should not appear in combo boxes. [Required] [Default(false)] [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccountGroup](Finance.Accounting.Accounts.md#AccountGroup) | [Finance.Accounting.AccountGroups](Finance.Accounting.AccountGroups.md) | The account group to which this account belongs. [Required] [Filter(multi eq)] |
| [Currency](Finance.Accounting.Accounts.md#Currency) | [General.Currencies](General.Currencies.md) (nullable) | The primary currency of the account. All movements on the account are stored in this currency. If there are movements on the account, the currency cannot be changed. [Filter(multi eq)] |
| [EnterpriseCompany](Finance.Accounting.Accounts.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this Account applies, or null if it is for all enterprise companies. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| RequiredProperties | [Finance.Accounting.AccountRequiredProperties](Finance.Accounting.AccountRequiredProperties.md) | List of [AccountRequiredProperty](Finance.Accounting.AccountRequiredProperties.md) child objects, based on the [Finance.Accounting.AccountRequiredProperty.Account](Finance.Accounting.AccountRequiredProperties.md#Account) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AccountFullNumber

> The full number of the account, unique among all accounts. It consists of the group number, concatenated with the account number. [Required] [Filter(like)] [ReadOnly]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Name

> The account name. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Number

> The number of the account, unique within the account group. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### CurrencyValuationMethod

> Method for base currency valuation of non base currency amounts. ACB = Account_Current_Balance, DCD = Document_Currency_Directory, BRD=Balance_Reference_Document. [Required] [Default("ACB")]

_Type_: **[Finance.Accounting.AccountsRepository.CurrencyValuationMethod](Finance.Accounting.Accounts.md#CurrencyValuationMethod)**  
Allowed values for the [CurrencyValuationMethod](Finance.Accounting.Accounts.md#CurrencyValuationMethod) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| AccountCurrentBalance | AccountCurrentBalance value. Stored as 'ACB'. <br /> _Database Value:_ 'ACB' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AccountCurrentBalance' |
| DocumentCurrencyDirectory | DocumentCurrencyDirectory value. Stored as 'DCD'. <br /> _Database Value:_ 'DCD' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'DocumentCurrencyDirectory' |
| BalanceReferenceDocument | BalanceReferenceDocument value. Stored as 'BRD'. <br /> _Database Value:_ 'BRD' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'BalanceReferenceDocument' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **AccountCurrentBalance**  

### Description

> The description of this Account.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Discontinued

> True means that the account won't be used any more and should not appear in combo boxes. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### AccountGroup

> The account group to which this account belongs. [Required] [Filter(multi eq)]

_Type_: **[Finance.Accounting.AccountGroups](Finance.Accounting.AccountGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Currency

> The primary currency of the account. All movements on the account are stored in this currency. If there are movements on the account, the currency cannot be changed. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> The Enterprise Company to which this Account applies, or null if it is for all enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Accounting.Accounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Accounting.Accounts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Accounting.Accounts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_Accounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_Accounts?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Acc_Accounts?$top=10>

