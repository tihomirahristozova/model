# Finance.Accounting.FinancialStatementNodes

Contains the hierarchical structure of the user-defined financial statements. Entity: Acc_Financial_Statement_Nodes

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Accounting.FinancialStatementNodes.md#Id) | guid |  
| [Code](Finance.Accounting.FinancialStatementNodes.md#Code) | string | Identifying code of the financial statement node. Unique within the parent financial statement node. [Required] [Filter(eq;like)] 
| [Name](Finance.Accounting.FinancialStatementNodes.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | Name of the financial statement node. [Required] [Filter(like)] 
| [FullPath](Finance.Accounting.FinancialStatementNodes.md#FullPath) | string (nullable) | Full identification path of the financial statement node. [Filter(like)] [ReadOnly] 
| [ParentFullPath](Finance.Accounting.FinancialStatementNodes.md#ParentFullPath) | string (nullable) | Parent financial statement node specified through its full identification path. [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [FinancialStatement](Finance.Accounting.FinancialStatementNodes.md#FinancialStatement) | [Finance.Accounting.FinancialStatements](Finance.Accounting.FinancialStatements.md) | The [FinancialStatement](Finance.Accounting.FinancialStatementNodes.md#FinancialStatement) to which this FinancialStatementNode belongs. [Required] [Filter(multi eq)] [Owner] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Correspondances | [Finance.Accounting.FinancialStatementNodeCorrespondances](Finance.Accounting.FinancialStatementNodeCorrespondances.md) | List of [FinancialStatementNodeCorrespondance](Finance.Accounting.FinancialStatementNodeCorrespondances.md) child objects, based on the [Finance.Accounting.FinancialStatementNodeCorrespondance.FinancialStatementNode](Finance.Accounting.FinancialStatementNodeCorrespondances.md#FinancialStatementNode) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> Identifying code of the financial statement node. Unique within the parent financial statement node. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Name

> Name of the financial statement node. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### FullPath

> Full identification path of the financial statement node. [Filter(like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ParentFullPath

> Parent financial statement node specified through its full identification path. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### FinancialStatement

> The [FinancialStatement](Finance.Accounting.FinancialStatementNodes.md#FinancialStatement) to which this FinancialStatementNode belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Accounting.FinancialStatements](Finance.Accounting.FinancialStatements.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



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

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Acc_Financial_Statement_Nodes?$top=10>

