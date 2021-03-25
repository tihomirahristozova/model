---
uid: Finance.Payments.PaymentTypes
---
# Finance.Payments.PaymentTypes Entity

**Namespace:** [Finance.Payments](Finance.Payments.md)  

Describes the way of payment. For example: in cash, by bank transfer, with credit card, etc. Entity: Cash_Payment_Types

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Payments.PaymentTypes.md#code) | string(16) | The payment type unique code. `Required` `Filter(eq;like)` `ORD` 
| [Id](Finance.Payments.PaymentTypes.md#id) | guid |  
| [IsActive](Finance.Payments.PaymentTypes.md#isactive) | boolean | Indicates wheather the payment type is active and usable for choosing in new documents. `Required` `Default(true)` `Filter(eq)` `Introduced in version 19.1` 
| [Name](Finance.Payments.PaymentTypes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this PaymentType. `Required` `Filter(like)` `ORD` 
| [SystemType](Finance.Payments.PaymentTypes.md#systemtype) | [SystemType](Finance.Payments.PaymentTypes.md#systemtype) (nullable) | Not null only when this is one of the system payment types. CS=Cash; CD=By Card; BT=Bank Transfer. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultPaymentAccount](Finance.Payments.PaymentTypes.md#defaultpaymentaccount) | [PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | When not null specifies the default payment account to use associated with this payment type. `Filter(multi eq)` |
| [EnterpriseCompany](Finance.Payments.PaymentTypes.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this PaymentType applies, or null if it is for all enterprise companies. `Filter(multi eq)` |


## Attribute Details

### Code

The payment type unique code. `Required` `Filter(eq;like)` `ORD`

_Type_: **string(16)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **16**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Indicates wheather the payment type is active and usable for choosing in new documents. `Required` `Default(true)` `Filter(eq)` `Introduced in version 19.1`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

The name of this PaymentType. `Required` `Filter(like)` `ORD`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Indexed_: **True**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  

### SystemType

Not null only when this is one of the system payment types. CS=Cash; CD=By Card; BT=Bank Transfer.

_Type_: **[SystemType](Finance.Payments.PaymentTypes.md#systemtype) (nullable)**  
Allowed values for the `SystemType`(Finance.Payments.PaymentTypes.md#systemtype) data attribute  
_Allowed Values (Finance.Payments.PaymentTypesRepository.SystemType Enum Members)_  

| Value | Description |
| ---- | --- |
| Cash | Cash value. Stored as 'CH'. <br /> _Database Value:_ 'CH' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Cash' |
| ByCard | ByCard value. Stored as 'CD'. <br /> _Database Value:_ 'CD' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'ByCard' |
| BankTransfer | BankTransfer value. Stored as 'BT'. <br /> _Database Value:_ 'BT' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'BankTransfer' |
| Coupons | Coupons value. Stored as 'TK'. <br /> _Database Value:_ 'TK' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Coupons' |
| Check | Check value. Stored as 'CK'. <br /> _Database Value:_ 'CK' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Check' |
| UserDefined1 | UserDefined1 value. Stored as 'U1'. <br /> _Database Value:_ 'U1' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'UserDefined1' |
| UserDefined2 | UserDefined2 value. Stored as 'U2'. <br /> _Database Value:_ 'U2' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'UserDefined2' |
| Vouchers | Vouchers value. Stored as 'U3'. <br /> _Database Value:_ 'U3' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'Vouchers' |
| Packaging | Packaging value. Stored as 'PK'. <br /> _Database Value:_ 'PK' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'Packaging' |
| InternalUsage | InternalUsage value. Stored as 'IU'. <br /> _Database Value:_ 'IU' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'InternalUsage' |
| Damage | Damage value. Stored as 'DG'. <br /> _Database Value:_ 'DG' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Damage' |
| Other | Other value. Stored as 'OT'. <br /> _Database Value:_ 'OT' <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'Other' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### DefaultPaymentAccount

When not null specifies the default payment account to use associated with this payment type. `Filter(multi eq)`

_Type_: **[PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

The Enterprise Company to which this PaymentType applies, or null if it is for all enterprise companies. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Payments.PaymentTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Payments.PaymentTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_PaymentTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_PaymentTypes?$top=10>

