---
uid: Logistics.Inventory.CostCorrectionLines
---
# Logistics.Inventory.CostCorrectionLines

Cost correction detail lines. One line is created for each corrected transaction line. Entity: Inv_Cost_Correction_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.CostCorrectionLines.md#Id) | guid |  
| [BaseCostAdjustment](Logistics.Inventory.CostCorrectionLines.md#BaseCostAdjustment) | [Amount](../data-types.md#Amount) | The amount of correction (plus or minus) for the Base Cost field of the transaction line. [Currency: TransactionLine.TransactionObj.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 
| [CostCorrectionAmount](Logistics.Inventory.CostCorrectionLines.md#CostCorrectionAmount) | [Amount](../data-types.md#Amount) | The amount of correction (plus or minus) for the Amount field of the transaction line. [Currency: TransactionLine.TransactionObj.DocumentCurrency] [Required] [Default(0)] 
| [ProductCostAdjustment](Logistics.Inventory.CostCorrectionLines.md#ProductCostAdjustment) | [Amount](../data-types.md#Amount) | The amount of correction (plus or minus) for the Product Cost field of the transaction line. [Currency: TransactionLine.Product.CostingCurrency] [Required] [Default(0)] 
| [StoreCostAdjustment](Logistics.Inventory.CostCorrectionLines.md#StoreCostAdjustment) | [Amount](../data-types.md#Amount) | The amount of correction (plus or minus) for the Store Cost field of the transaction line. [Currency: TransactionLine.TransactionObj.Store.Currency] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CostCorrection](Logistics.Inventory.CostCorrectionLines.md#CostCorrection) | [Logistics.Inventory.CostCorrections](Logistics.Inventory.CostCorrections.md) | The [CostCorrection](Logistics.Inventory.CostCorrectionLines.md#CostCorrection) to which this CostCorrectionLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [TransactionLine](Logistics.Inventory.CostCorrectionLines.md#TransactionLine) | [Logistics.Inventory.StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md) | The transaction line, which is corrected. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### BaseCostAdjustment

> The amount of correction (plus or minus) for the Base Cost field of the transaction line. [Currency: TransactionLine.TransactionObj.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### CostCorrectionAmount

> The amount of correction (plus or minus) for the Amount field of the transaction line. [Currency: TransactionLine.TransactionObj.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ProductCostAdjustment

> The amount of correction (plus or minus) for the Product Cost field of the transaction line. [Currency: TransactionLine.Product.CostingCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### StoreCostAdjustment

> The amount of correction (plus or minus) for the Store Cost field of the transaction line. [Currency: TransactionLine.TransactionObj.Store.Currency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### CostCorrection

> The [CostCorrection](Logistics.Inventory.CostCorrectionLines.md#CostCorrection) to which this CostCorrectionLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Inventory.CostCorrections](Logistics.Inventory.CostCorrections.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TransactionLine

> The transaction line, which is corrected. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.CostCorrectionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.CostCorrectionLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.CostCorrectionLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_CostCorrectionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_CostCorrectionLines?$top=10>

