# Finance.Accounting.AccountingVoucherLines

Contains one debit or credit posting within an accounting voucher. Entity: Acc_Voucher_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Accounting.AccountingVoucherLines.md#Id) | guid |  
| [CorrespondanceNo](Finance.Accounting.AccountingVoucherLines.md#CorrespondanceNo) | int32 | The number of the correspondance group within the accounting voucher. For each correspondance group, the debits are equal to the credits. [Required] [Default(0)] 
| [CorrespondantAmount](Finance.Accounting.AccountingVoucherLines.md#CorrespondantAmount) | decimal (nullable) | The amount (in the currency of the correspondant line) to which the amount in this line is corresponding. This field has value only when the current line is corresponding to only one line (e.g. null means that the current line is corresponding to many lines). [ReadOnly] 
| [Credit](Finance.Accounting.AccountingVoucherLines.md#Credit) | [Amount](../data-types/Amount.md) | The amount of the credit in the currency of the account. 0 means that the account is not credited. [Currency: Currency] [Required] [Default(0)] 
| [CreditBase](Finance.Accounting.AccountingVoucherLines.md#CreditBase) | [Amount](../data-types/Amount.md) | The amount of credit in base currency. [Currency: Voucher.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 
| [Debit](Finance.Accounting.AccountingVoucherLines.md#Debit) | [Amount](../data-types/Amount.md) | The amount of the debit in the currency of the account. 0 means that the account is not debited. [Currency: Currency] [Required] [Default(0)] 
| [DebitBase](Finance.Accounting.AccountingVoucherLines.md#DebitBase) | [Amount](../data-types/Amount.md) | The amount of debit in base currency. [Currency: Voucher.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 
| [ItemKey](Finance.Accounting.AccountingVoucherLines.md#ItemKey) | string (nullable) | The item (grouping) key for the account in the line. Account_Id + Item_Key - the smallest unit of calculation for account balance. [Filter(eq;like)] 
| [LineNo](Finance.Accounting.AccountingVoucherLines.md#LineNo) | int32 | Consecutive number of the line within the voucher. [Required] 
| [RateDivisor](Finance.Accounting.AccountingVoucherLines.md#RateDivisor) | decimal | The divisor for conversion from Debit/Credit to base currency. [Required] [Default(1)] 
| [RateMultiplier](Finance.Accounting.AccountingVoucherLines.md#RateMultiplier) | decimal | The multiplier for conversion from Debit/Credit to base currency. [Required] [Default(1)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Account](Finance.Accounting.AccountingVoucherLines.md#Account) | [Finance.Accounting.Accounts](Finance.Accounting.Accounts.md) | The account being debited or credited. [Required] [Filter(multi eq)] |
| [CostCenter](Finance.Accounting.AccountingVoucherLines.md#CostCenter) | [Finance.Accounting.CostCenters](Finance.Accounting.CostCenters.md) (nullable) | The cost center to which this cost is related. [Filter(multi eq)] |
| [Currency](Finance.Accounting.AccountingVoucherLines.md#Currency) | [General.Currencies](General.Currencies.md) | The currency of the movement in this line. If there is defined currency for the account in the line that it should be equal to the value in this field. [Required] [Filter(multi eq)] |
| [ProfitCenter](Finance.Accounting.AccountingVoucherLines.md#ProfitCenter) | [Finance.Accounting.ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable) | The profit center to which this revenue is related. [Filter(multi eq)] |
| [ReferencedDocument](Finance.Accounting.AccountingVoucherLines.md#ReferencedDocument) | [General.Documents](General.Documents.md) | The document which is referenced by the line. By default, this is the document of the voucher. [Required] [Filter(multi eq)] |
| [Voucher](Finance.Accounting.AccountingVoucherLines.md#Voucher) | [Finance.Accounting.AccountingVouchers](Finance.Accounting.AccountingVouchers.md) | The voucher to which this line is attached. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CorrespondanceNo

> The number of the correspondance group within the accounting voucher. For each correspondance group, the debits are equal to the credits. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### CorrespondantAmount

> The amount (in the currency of the correspondant line) to which the amount in this line is corresponding. This field has value only when the current line is corresponding to only one line (e.g. null means that the current line is corresponding to many lines). [ReadOnly]

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Credit

> The amount of the credit in the currency of the account. 0 means that the account is not credited. [Currency: Currency] [Required] [Default(0)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### CreditBase

> The amount of credit in base currency. [Currency: Voucher.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Debit

> The amount of the debit in the currency of the account. 0 means that the account is not debited. [Currency: Currency] [Required] [Default(0)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### DebitBase

> The amount of debit in base currency. [Currency: Voucher.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ItemKey

> The item (grouping) key for the account in the line. Account_Id + Item_Key - the smallest unit of calculation for account balance. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### LineNo

> Consecutive number of the line within the voucher. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.Voucher.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.Voucher.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### RateDivisor

> The divisor for conversion from Debit/Credit to base currency. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### RateMultiplier

> The multiplier for conversion from Debit/Credit to base currency. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### Account

> The account being debited or credited. [Required] [Filter(multi eq)]

_Type_: **[Finance.Accounting.Accounts](Finance.Accounting.Accounts.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### CostCenter

> The cost center to which this cost is related. [Filter(multi eq)]

_Type_: **[Finance.Accounting.CostCenters](Finance.Accounting.CostCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Currency

> The currency of the movement in this line. If there is defined currency for the account in the line that it should be equal to the value in this field. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProfitCenter

> The profit center to which this revenue is related. [Filter(multi eq)]

_Type_: **[Finance.Accounting.ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ReferencedDocument

> The document which is referenced by the line. By default, this is the document of the voucher. [Required] [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Voucher

> The voucher to which this line is attached. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Accounting.AccountingVouchers](Finance.Accounting.AccountingVouchers.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Accounting.AccountingVoucherLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Accounting.AccountingVoucherLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Accounting.AccountingVoucherLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_AccountingVoucherLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_AccountingVoucherLines?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Acc_Voucher_Lines?$top=10>

