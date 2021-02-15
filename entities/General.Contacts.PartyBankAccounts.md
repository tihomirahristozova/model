---
uid: General.Contacts.PartyBankAccounts
---
# General.Contacts.PartyBankAccounts Entity

The bank accounts of a party. Entity: Gen_Party_Bank_Accounts

Default Display Text Format:  
_{BankAccountCode}: {BankBranchName:T}_  
Default Search Member:  
_BankAccountCode_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BankAccountCode](General.Contacts.PartyBankAccounts.md#bankaccountcode) | string | The code of the account, usually the IBAN code. [Required] [Filter(eq;like)] 
| [BankAddress](General.Contacts.PartyBankAccounts.md#bankaddress) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | The address of the bank or the bank branch office. Required (not-null) only for own accounts for printing or exporting bank payments. 
| [BankBranchName](General.Contacts.PartyBankAccounts.md#bankbranchname) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | The name of the branch office of the bank, where the account is located. Required (not-null) only for own accounts for printing or exporting bank payments. 
| [BankCode](General.Contacts.PartyBankAccounts.md#bankcode) | string (nullable) | The code of the bank, usually the BIC code. [Filter(eq)] 
| [BankName](General.Contacts.PartyBankAccounts.md#bankname) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | The full name of the bank. [Filter(like)] 
| [Id](General.Contacts.PartyBankAccounts.md#id) | guid |  
| [IsDefault](General.Contacts.PartyBankAccounts.md#isdefault) | boolean | True if the this is the default account for the party. Only one default per party is allowed. [Required] [Default(false)] [Filter(eq)] 
| [Notes](General.Contacts.PartyBankAccounts.md#notes) | string (nullable) | Notes for this PartyBankAccount. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Party](General.Contacts.PartyBankAccounts.md#party) | [Parties](General.Contacts.Parties.md) | The [Party](General.Contacts.PartyBankAccounts.md#party) to which this PartyBankAccount belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### BankAccountCode

The code of the account, usually the IBAN code. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### BankAddress

The address of the bank or the bank branch office. Required (not-null) only for own accounts for printing or exporting bank payments.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### BankBranchName

The name of the branch office of the bank, where the account is located. Required (not-null) only for own accounts for printing or exporting bank payments.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### BankCode

The code of the bank, usually the BIC code. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### BankName

The full name of the bank. [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDefault

True if the this is the default account for the party. Only one default per party is allowed. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

Notes for this PartyBankAccount.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Party

The [Party](General.Contacts.PartyBankAccounts.md#party) to which this PartyBankAccount belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.PartyBankAccounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.PartyBankAccounts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_PartyBankAccounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_PartyBankAccounts?$top=10>

