---
uid: Finance.Accounting.FinancialStatementNodes
---
# Finance.Accounting.FinancialStatementNodes Entity

**Namespace:** [Finance.Accounting](Finance.Accounting.md)  

Contains the hierarchical structure of the user-defined financial statements. Entity: Acc_Financial_Statement_Nodes

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Code; Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Accounting.FinancialStatements](Finance.Accounting.FinancialStatements.md)  
Aggregate Root:  
[Finance.Accounting.FinancialStatements](Finance.Accounting.FinancialStatements.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Accounting.FinancialStatementNodes.md#code) | string (3) | Identifying code of the financial statement node. Unique within the parent financial statement node. `Required` `Filter(eq;like)` 
| [FullPath](Finance.Accounting.FinancialStatementNodes.md#fullpath) | string (25) __nullable__ | Full identification path of the financial statement node. `Filter(like)` `ReadOnly` 
| [Id](Finance.Accounting.FinancialStatementNodes.md#id) | guid |  
| [Name](Finance.Accounting.FinancialStatementNodes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the financial statement node. `Required` `Filter(like)` 
| [ObjectVersion](Finance.Accounting.FinancialStatementNodes.md#objectversion) | int32 |  
| [ParentFullPath](Finance.Accounting.FinancialStatementNodes.md#parentfullpath) | string (25) __nullable__ | Parent financial statement node specified through its full identification path. `Filter(like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [FinancialStatement](Finance.Accounting.FinancialStatementNodes.md#financialstatement) | [FinancialStatements](Finance.Accounting.FinancialStatements.md) | The <see cref="Financial<br />Statement"/> to which this FinancialStatementNode belongs. `Required` `Filter(multi eq)` `Owner` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Correspondances | [FinancialStatementNodeCorrespondances](Finance.Accounting.FinancialStatementNodeCorrespondances.md) | List of `FinancialStatement<br />NodeCorrespondance`(Finance.Accounting.FinancialStatement<br />NodeCorrespondances.md) child objects, based on the `Finance.Accounting.FinancialStatement<br />NodeCorrespondance.FinancialStatementNode`(Finance.Accounting.FinancialStatement<br />NodeCorrespondances.md#financialstatementnode) back reference 


## Attribute Details

### Code

Identifying code of the financial statement node. Unique within the parent financial statement node. `Required` `Filter(eq;like)`

_Type_: **string (3)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **3**  

### FullPath

Full identification path of the financial statement node. `Filter(like)` `ReadOnly`

_Type_: **string (25) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **25**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the financial statement node. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ParentFullPath

Parent financial statement node specified through its full identification path. `Filter(like)`

_Type_: **string (25) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **25**  


## Reference Details

### FinancialStatement

The <see cref="FinancialStatement"/> to which this FinancialStatementNode belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[FinancialStatements](Finance.Accounting.FinancialStatements.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.FinancialStatementNodes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.FinancialStatementNodes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_FinancialStatementNodes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_FinancialStatementNodes?$top=10>

