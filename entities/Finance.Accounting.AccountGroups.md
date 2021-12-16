---
uid: Finance.Accounting.AccountGroups
---
# Finance.Accounting.AccountGroups Entity

**Namespace:** [Finance.Accounting](Finance.Accounting.md)  

Hierarchical chart of account groups. Entity: Acc_Account_Groups

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Number; Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Accounting.AccountGroups](Finance.Accounting.AccountGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](Finance.Accounting.AccountGroups.md#description) | [MultilanguageString](../data-types.md#multilanguagestring) __nullable__ | The description of this AccountGroup. 
| [Discontinued](Finance.Accounting.AccountGroups.md#discontinued) | boolean | True means that the account group won't be used any more and should not appear in combo boxes. `Required` `Default(false)` `Filter(eq)` 
| [FullPath](Finance.Accounting.AccountGroups.md#fullpath) | string (256) __nullable__ | Full path to the group. Contains delimited list of group numbers of parent groups. `Filter(like)` 
| [Id](Finance.Accounting.AccountGroups.md#id) | guid |  
| [Name](Finance.Accounting.AccountGroups.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Account group name, required. Must be unique within the parent group. `Required` `Filter(like)` 
| [Number](Finance.Accounting.AccountGroups.md#number) | string (30) | Unique account group number. May contain characters, if required. `Required` `Filter(like)` `ORD` 
| [RowVersion](Finance.Accounting.AccountGroups.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Finance.Accounting.AccountGroups.md#parent) | [AccountGroups](Finance.Accounting.AccountGroups.md) (nullable) | Parent account group. null if this is root group. `Filter(multi eq)` |


## Attribute Details

### Description

The description of this AccountGroup.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Discontinued

True means that the account group won't be used any more and should not appear in combo boxes. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### FullPath

Full path to the group. Contains delimited list of group numbers of parent groups. `Filter(like)`

_Type_: **string (256) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **256**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Account group name, required. Must be unique within the parent group. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Number

Unique account group number. May contain characters, if required. `Required` `Filter(like)` `ORD`

_Type_: **string (30)**  
_Indexed_: **True**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  
_Maximum Length_: **30**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Parent

Parent account group. null if this is root group. `Filter(multi eq)`

_Type_: **[AccountGroups](Finance.Accounting.AccountGroups.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.AccountGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.AccountGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_AccountGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_AccountGroups?$top=10>

