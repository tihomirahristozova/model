---
uid: Logistics.Inventory.TransactionCostCorrectionsSummary
---
# Logistics.Inventory.TransactionCostCorrectionsSummary

Summary of cost corrections, grouped by the line corrected. Entity: Inv_Transaction_Cost_Corrections_Summary

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BaseCostAdjustment](Logistics.Inventory.TransactionCostCorrectionsSummary.md#BaseCostAdjustment) | [Amount](../data-types.md#Amount) | The cost correction in Base currency. [Currency: TransactionObj.EnterpriseCompany.BaseCurrency] [Required] [Filter(eq;ge;le)] 
| [CostCorrectionAmount](Logistics.Inventory.TransactionCostCorrectionsSummary.md#CostCorrectionAmount) | [Amount](../data-types.md#Amount) | The cost correction in the original currency of the store transaction. [Currency: TransactionObj.DocumentCurrency] [Required] [Filter(eq;ge;le)] 
| [ProductCostAdjustment](Logistics.Inventory.TransactionCostCorrectionsSummary.md#ProductCostAdjustment) | [Amount](../data-types.md#Amount) | The cost correction in Products currency. [Currency: TransactionLine.Product.CostingCurrency] [Required] [Filter(eq;ge;le)] 
| [StoreCostAdjustment](Logistics.Inventory.TransactionCostCorrectionsSummary.md#StoreCostAdjustment) | [Amount](../data-types.md#Amount) | The cost correction in Stores currency. [Currency: TransactionObj.Store.Currency] [Required] [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [TransactionObj](Logistics.Inventory.TransactionCostCorrectionsSummary.md#TransactionObj) | [Logistics.Inventory.StoreTransactions](Logistics.Inventory.StoreTransactions.md) | The transaction to which the transaction line belongs. [Required] [Filter(multi eq)] [Owner] |
| [TransactionLine](Logistics.Inventory.TransactionCostCorrectionsSummary.md#TransactionLine) | [Logistics.Inventory.StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md) | Unique transaction line id. [Required] [Default(New Guid)] [Filter(multi eq)] |


## Attribute Details

### BaseCostAdjustment

> The cost correction in Base currency. [Currency: TransactionObj.EnterpriseCompany.BaseCurrency] [Required] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CostCorrectionAmount

> The cost correction in the original currency of the store transaction. [Currency: TransactionObj.DocumentCurrency] [Required] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ProductCostAdjustment

> The cost correction in Products currency. [Currency: TransactionLine.Product.CostingCurrency] [Required] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### StoreCostAdjustment

> The cost correction in Stores currency. [Currency: TransactionObj.Store.Currency] [Required] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### TransactionObj

> The transaction to which the transaction line belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Inventory.StoreTransactions](Logistics.Inventory.StoreTransactions.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TransactionLine

> Unique transaction line id. [Required] [Default(New Guid)] [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  



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

