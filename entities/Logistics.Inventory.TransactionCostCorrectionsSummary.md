---
uid: Logistics.Inventory.TransactionCostCorrectionsSummary
---
# Logistics.Inventory.TransactionCostCorrectionsSummary Entity

Summary of cost corrections, grouped by the line corrected. Entity: Inv_Transaction_Cost_Corrections_Summary

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BaseCostAdjustment](Logistics.Inventory.TransactionCostCorrectionsSummary.md#basecostadjustment) | [Amount](../data-types.md#amount) | The cost correction in Base currency. [Currency: TransactionObj.EnterpriseCompany.BaseCurrency] [Required] [Filter(eq;ge;le)] 
| [CostCorrectionAmount](Logistics.Inventory.TransactionCostCorrectionsSummary.md#costcorrectionamount) | [Amount](../data-types.md#amount) | The cost correction in the original currency of the store transaction. [Currency: TransactionObj.DocumentCurrency] [Required] [Filter(eq;ge;le)] 
| [ProductCostAdjustment](Logistics.Inventory.TransactionCostCorrectionsSummary.md#productcostadjustment) | [Amount](../data-types.md#amount) | The cost correction in Products currency. [Currency: TransactionLine.Product.CostingCurrency] [Required] [Filter(eq;ge;le)] 
| [StoreCostAdjustment](Logistics.Inventory.TransactionCostCorrectionsSummary.md#storecostadjustment) | [Amount](../data-types.md#amount) | The cost correction in Stores currency. [Currency: TransactionObj.Store.Currency] [Required] [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [TransactionLine](Logistics.Inventory.TransactionCostCorrectionsSummary.md#transactionline) | [StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md) | Unique transaction line id. [Required] [Default(New Guid)] [Filter(multi eq)] |
| [TransactionObj](Logistics.Inventory.TransactionCostCorrectionsSummary.md#transactionobj) | [StoreTransactions](Logistics.Inventory.StoreTransactions.md) | The transaction to which the transaction line belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### BaseCostAdjustment

The cost correction in Base currency. [Currency: TransactionObj.EnterpriseCompany.BaseCurrency] [Required] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CostCorrectionAmount

The cost correction in the original currency of the store transaction. [Currency: TransactionObj.DocumentCurrency] [Required] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ProductCostAdjustment

The cost correction in Products currency. [Currency: TransactionLine.Product.CostingCurrency] [Required] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### StoreCostAdjustment

The cost correction in Stores currency. [Currency: TransactionObj.Store.Currency] [Required] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### TransactionLine

Unique transaction line id. [Required] [Default(New Guid)] [Filter(multi eq)]

_Type_: **[StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### TransactionObj

The transaction to which the transaction line belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[StoreTransactions](Logistics.Inventory.StoreTransactions.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Inventory.TransactionCostCorrectionsSummary erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.TransactionCostCorrectionsSummary erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.TransactionCostCorrectionsSummary erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_TransactionCostCorrectionsSummary?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_TransactionCostCorrectionsSummary?$top=10>

