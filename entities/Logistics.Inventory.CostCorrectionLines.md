---
uid: Logistics.Inventory.CostCorrectionLines
---
# Logistics.Inventory.CostCorrectionLines Entity

**Namespace:** [Logistics.Inventory](Logistics.Inventory.md)  

Cost correction detail lines. One line is created for each corrected transaction line. Entity: Inv_Cost_Correction_Lines

## Default Visualization
Default Display Text Format:  
_{CostCorrection.DocumentType.Code}:{CostCorrection.DocumentNo} - {CostCorrection.DocumentType.TypeName:T}_  
Default Search Member:  
_CostCorrection.DocumentType.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Inventory.CostCorrections](Logistics.Inventory.CostCorrections.md)  
Aggregate Root:  
[Logistics.Inventory.CostCorrections](Logistics.Inventory.CostCorrections.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BaseCostAdjustment](Logistics.Inventory.CostCorrectionLines.md#basecostadjustment) | [Amount](../data-types.md#amount) | The amount of correction (plus or minus) for the Base Cost field of the transaction line. [Currency: TransactionLine.TransactionObj.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 
| [CostCorrectionAmount](Logistics.Inventory.CostCorrectionLines.md#costcorrectionamount) | [Amount](../data-types.md#amount) | The amount of correction (plus or minus) for the Amount field of the transaction line. [Currency: TransactionLine.TransactionObj.DocumentCurrency] [Required] [Default(0)] 
| [Id](Logistics.Inventory.CostCorrectionLines.md#id) | guid |  
| [ProductCostAdjustment](Logistics.Inventory.CostCorrectionLines.md#productcostadjustment) | [Amount](../data-types.md#amount) | The amount of correction (plus or minus) for the Product Cost field of the transaction line. [Currency: TransactionLine.Product.CostingCurrency] [Required] [Default(0)] 
| [StoreCostAdjustment](Logistics.Inventory.CostCorrectionLines.md#storecostadjustment) | [Amount](../data-types.md#amount) | The amount of correction (plus or minus) for the Store Cost field of the transaction line. [Currency: TransactionLine.TransactionObj.Store.Currency] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CostCorrection](Logistics.Inventory.CostCorrectionLines.md#costcorrection) | [CostCorrections](Logistics.Inventory.CostCorrections.md) | The [CostCorrection](Logistics.Inventory.CostCorrectionLines.md#costcorrection) to which this CostCorrectionLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [TransactionLine](Logistics.Inventory.CostCorrectionLines.md#transactionline) | [StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md) | The transaction line, which is corrected. [Required] [Filter(multi eq)] |


## Attribute Details

### BaseCostAdjustment

The amount of correction (plus or minus) for the Base Cost field of the transaction line. [Currency: TransactionLine.TransactionObj.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### CostCorrectionAmount

The amount of correction (plus or minus) for the Amount field of the transaction line. [Currency: TransactionLine.TransactionObj.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ProductCostAdjustment

The amount of correction (plus or minus) for the Product Cost field of the transaction line. [Currency: TransactionLine.Product.CostingCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### StoreCostAdjustment

The amount of correction (plus or minus) for the Store Cost field of the transaction line. [Currency: TransactionLine.TransactionObj.Store.Currency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### CostCorrection

The [CostCorrection](Logistics.Inventory.CostCorrectionLines.md#costcorrection) to which this CostCorrectionLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[CostCorrections](Logistics.Inventory.CostCorrections.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### TransactionLine

The transaction line, which is corrected. [Required] [Filter(multi eq)]

_Type_: **[StoreTransactionLines](Logistics.Inventory.StoreTransactionLines.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Inventory.CostCorrectionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.CostCorrectionLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_CostCorrectionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_CostCorrectionLines?$top=10>

