---
uid: Finance.Accounting.FinancialStatementNodeCorrespondances
---
# Finance.Accounting.FinancialStatementNodeCorrespondances Entity

**Namespace:** [Finance.Accounting](Finance.Accounting.md)  

Contains the actual correspondance filters, which specify how each financial statement node is calculated. Entity: Acc_Financial_Statement_Node_Correspondances

## Default Visualization
Default Display Text Format:  
_{FinancialStatementNode.Name:T} : {FinancialStatementNode.Code}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Accounting.FinancialStatementNodes](Finance.Accounting.FinancialStatementNodes.md)  
Aggregate Root:  
[Finance.Accounting.FinancialStatements](Finance.Accounting.FinancialStatements.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Accounting.FinancialStatementNodeCorrespondances.md#id) | guid |  
| [Multiplier](Finance.Accounting.FinancialStatementNodeCorrespondances.md#multiplier) | decimal (18, 0) | Factor by which the correspondence balance will be multiplied. `Required` `Default(1)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccountGroup](Finance.Accounting.FinancialStatementNodeCorrespondances.md#accountgroup) | [AccountGroups](Finance.Accounting.AccountGroups.md) | Main account group determining the correspondances for which the balances are summed. `Required` `Filter(multi eq)` |
| [CorrespondantAccountGroup](Finance.Accounting.FinancialStatementNodeCorrespondances.md#correspondantaccountgroup) | [AccountGroups](Finance.Accounting.AccountGroups.md) (nullable) | Correspondant account group determining the correspondances for which the balances are summed. If null means that the balances of all correspondances for the main account group are summed. `Filter(multi eq)` |
| [FinancialStatementNode](Finance.Accounting.FinancialStatementNodeCorrespondances.md#financialstatementnode) | [FinancialStatementNodes](Finance.Accounting.FinancialStatementNodes.md) | The `FinancialStatementNode`(Finance.Accounting.FinancialStatement<br />NodeCorrespondances.md#financialstatementnode) to which this FinancialStatement<br />NodeCorrespondance belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Multiplier

Factor by which the correspondence balance will be multiplied. `Required` `Default(1)`

_Type_: **decimal (18, 0)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### AccountGroup

Main account group determining the correspondances for which the balances are summed. `Required` `Filter(multi eq)`

_Type_: **[AccountGroups](Finance.Accounting.AccountGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### CorrespondantAccountGroup

Correspondant account group determining the correspondances for which the balances are summed. If null means that the balances of all correspondances for the main account group are summed. `Filter(multi eq)`

_Type_: **[AccountGroups](Finance.Accounting.AccountGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FinancialStatementNode

The `FinancialStatementNode`(Finance.Accounting.FinancialStatementNodeCorrespondances.md#financialstatementnode) to which this FinancialStatementNodeCorrespondance belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[FinancialStatementNodes](Finance.Accounting.FinancialStatementNodes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.FinancialStatementNodeCorrespondances erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.FinancialStatementNodeCorrespondances erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_FinancialStatementNodeCorrespondances?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_FinancialStatementNodeCorrespondances?$top=10>

