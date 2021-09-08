---
uid: Finance.Accounting.FinancialStatements
---
# Finance.Accounting.FinancialStatements Entity

**Namespace:** [Finance.Accounting](Finance.Accounting.md)  

Contains the user-defined financial statement definitions. Entity: Acc_Financial_Statements

## Default Visualization
Default Display Text Format:  
_{Name:T} #{Code}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Accounting.FinancialStatements](Finance.Accounting.FinancialStatements.md)  
  * [Finance.Accounting.FinancialStatementNodes](Finance.Accounting.FinancialStatementNodes.md)  
    * [Finance.Accounting.FinancialStatementNodeCorrespondances](Finance.Accounting.FinancialStatementNodeCorrespondances.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Accounting.FinancialStatements.md#code) | string (3) | Unique identifying code of the financial statement. `Required` `Filter(eq;like)` `ORD` 
| [Id](Finance.Accounting.FinancialStatements.md#id) | guid |  
| [Name](Finance.Accounting.FinancialStatements.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the financial statement. `Required` `Filter(eq;like)` 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Nodes | [FinancialStatementNodes](Finance.Accounting.FinancialStatementNodes.md) | List of `FinancialStatementNode`(Finance.Accounting.FinancialStatementNodes.md) child objects, based on the `Finance.Accounting.FinancialStatementNode.FinancialStatement`(Finance.Accounting.FinancialStatementNodes.md#financialstatement) back reference 


## Attribute Details

### Code

Unique identifying code of the financial statement. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (3)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **3**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the financial statement. `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.FinancialStatements erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Accounting.FinancialStatements erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_FinancialStatements?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_FinancialStatements?$top=10>

