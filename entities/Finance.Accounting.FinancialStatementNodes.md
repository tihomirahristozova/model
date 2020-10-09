---
uid: Finance.Accounting.FinancialStatementNodes
---
# Finance.Accounting.FinancialStatementNodes Entity

Contains the hierarchical structure of the user-defined financial statements. Entity: Acc_Financial_Statement_Nodes

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Accounting.FinancialStatementNodes.md#code) | string | Identifying code of the financial statement node. Unique within the parent financial statement node. [Required] [Filter(eq;like)] 
| [FullPath](Finance.Accounting.FinancialStatementNodes.md#fullpath) | string (nullable) | Full identification path of the financial statement node. [Filter(like)] [ReadOnly] 
| [Id](Finance.Accounting.FinancialStatementNodes.md#id) | guid |  
| [Name](Finance.Accounting.FinancialStatementNodes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the financial statement node. [Required] [Filter(like)] 
| [ParentFullPath](Finance.Accounting.FinancialStatementNodes.md#parentfullpath) | string (nullable) | Parent financial statement node specified through its full identification path. [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [FinancialStatement](Finance.Accounting.FinancialStatementNodes.md#financialstatement) | [FinancialStatements](Finance.Accounting.FinancialStatements.md) | The [FinancialStatement](Finance.Accounting.FinancialStatementNodes.md#financialstatement) to which this FinancialStatementNode belongs. [Required] [Filter(multi eq)] [Owner] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Correspondances | [FinancialStatementNodeCorrespondances](Finance.Accounting.FinancialStatementNodeCorrespondances.md) | List of [FinancialStatement<br />NodeCorrespondance](Finance.Accounting.FinancialStatement<br />NodeCorrespondances.md) child objects, based on the [Finance.Accounting.FinancialStatement<br />NodeCorrespondance.FinancialStatementNode](Finance.Accounting.FinancialStatement<br />NodeCorrespondances.md#financialstatementnode) back  


## Attribute Details

### Code

> Identifying code of the financial statement node. Unique within the parent financial statement node. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### FullPath

> Full identification path of the financial statement node. [Filter(like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> Name of the financial statement node. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ParentFullPath

> Parent financial statement node specified through its full identification path. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### FinancialStatement

> The [FinancialStatement](Finance.Accounting.FinancialStatementNodes.md#financialstatement) to which this FinancialStatementNode belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[FinancialStatements](Finance.Accounting.FinancialStatements.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Accounting.FinancialStatementNodes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Accounting.FinancialStatementNodes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Accounting.FinancialStatementNodes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_FinancialStatementNodes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_FinancialStatementNodes?$top=10>

