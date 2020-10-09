---
uid: Finance.Accounting.FinancialStatements
---
# Finance.Accounting.FinancialStatements

Contains the user-defined financial statement definitions. Entity: Acc_Financial_Statements

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Accounting.FinancialStatements.md#code) | string | Unique identifying code of the financial statement. [Required] [Filter(eq;like)] [ORD] 
| [Id](Finance.Accounting.FinancialStatements.md#id) | guid |  
| [Name](Finance.Accounting.FinancialStatements.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the financial statement. [Required] [Filter(eq;like)] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Nodes | [FinancialStatementNodes](Finance.Accounting.FinancialStatementNodes.md) | List of [FinancialStatementNode](Finance.Accounting.FinancialStatementNodes.md) child objects, based on the [Finance.Accounting.FinancialStatementNode.FinancialStatement](Finance.Accounting.FinancialStatementNodes.md#financialstatement) back reference 


## Attribute Details

### Code

> Unique identifying code of the financial statement. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> Name of the financial statement. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Accounting.FinancialStatements erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Accounting.FinancialStatements erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Accounting.FinancialStatements erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_FinancialStatements?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_FinancialStatements?$top=10>

