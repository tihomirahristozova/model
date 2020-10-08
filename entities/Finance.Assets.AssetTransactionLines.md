---
uid: Finance.Assets.AssetTransactionLines
---
# Finance.Assets.AssetTransactionLines

Asset value transaction lines. Each line changes the values of one asset in one valuation model. Entity: Ast_Asset_Transaction_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Assets.AssetTransactionLines.md#Id) | guid |  
| [DepreciationValue](Finance.Assets.AssetTransactionLines.md#DepreciationValue) | [Amount](../data-types.md#Amount) | Change in the depreciation value of the asset (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)] 
| [DepreciationValueBase](Finance.Assets.AssetTransactionLines.md#DepreciationValueBase) | [Amount](../data-types.md#Amount) | Change in the depreciation value of the asset (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 
| [NegativeReserveValue](Finance.Assets.AssetTransactionLines.md#NegativeReserveValue) | [Amount](../data-types.md#Amount) | Change in the value of the negative reserve after asset valuations (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)] 
| [NegativeReserveValueBase](Finance.Assets.AssetTransactionLines.md#NegativeReserveValueBase) | [Amount](../data-types.md#Amount) | Change in the value of the negative reserve after asset valuations (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 
| [OperationType](Finance.Assets.AssetTransactionLines.md#OperationType) | [Finance.Assets.AssetTransactionLinesRepository.OperationType](Finance.Assets.AssetTransactionLines.md#OperationType) | Type of the current asset operation: PUR = Purchase, SLS = Sale, DEP = Depreciation, ADJ = Adjustment, REV = Reevaluation. [Required] [Default("ADJ")] [Filter(multi eq)] 
| [PositiveReserveValue](Finance.Assets.AssetTransactionLines.md#PositiveReserveValue) | [Amount](../data-types.md#Amount) | Change in the value of the positive reserve after asset valuations (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)] 
| [PositiveReserveValueBase](Finance.Assets.AssetTransactionLines.md#PositiveReserveValueBase) | [Amount](../data-types.md#Amount) | Change in the value of the positive reserve after asset valuations (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 
| [PurchaseValue](Finance.Assets.AssetTransactionLines.md#PurchaseValue) | [Amount](../data-types.md#Amount) | Change in the purchase value of the asset (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)] 
| [PurchaseValueBase](Finance.Assets.AssetTransactionLines.md#PurchaseValueBase) | [Amount](../data-types.md#Amount) | Change in the purchase value of the asset (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 
| [SalvageValue](Finance.Assets.AssetTransactionLines.md#SalvageValue) | [Amount](../data-types.md#Amount) | Change in the salvage value of the asset (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)] 
| [SalvageValueBase](Finance.Assets.AssetTransactionLines.md#SalvageValueBase) | [Amount](../data-types.md#Amount) | Change in the salvage value of the asset (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Asset](Finance.Assets.AssetTransactionLines.md#Asset) | [Finance.Assets.Assets](Finance.Assets.Assets.md) | Asset for which changes in values have occurred. [Required] [Filter(multi eq)] |
| [AssetTransaction](Finance.Assets.AssetTransactionLines.md#AssetTransaction) | [Finance.Assets.AssetTransactions](Finance.Assets.AssetTransactions.md) | The [AssetTransaction](Finance.Assets.AssetTransactionLines.md#AssetTransaction) to which this AssetTransactionLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [ValuationModel](Finance.Assets.AssetTransactionLines.md#ValuationModel) | [Finance.Assets.ValuationModels](Finance.Assets.ValuationModels.md) | Valuation model in which the changes of the asset values have occurred (Taxation model or Accounting model or other). [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DepreciationValue

> Change in the depreciation value of the asset (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### DepreciationValueBase

> Change in the depreciation value of the asset (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### NegativeReserveValue

> Change in the value of the negative reserve after asset valuations (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### NegativeReserveValueBase

> Change in the value of the negative reserve after asset valuations (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### OperationType

> Type of the current asset operation: PUR = Purchase, SLS = Sale, DEP = Depreciation, ADJ = Adjustment, REV = Reevaluation. [Required] [Default("ADJ")] [Filter(multi eq)]

_Type_: **[Finance.Assets.AssetTransactionLinesRepository.OperationType](Finance.Assets.AssetTransactionLines.md#OperationType)**  
Allowed values for the [OperationType](Finance.Assets.AssetTransactionLines.md#OperationType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Adjustment | Adjustment value. Stored as 'ADJ'. <br /> _Database Value:_ 'ADJ' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Adjustment' |
| Depreciation | Depreciation value. Stored as 'DEP'. <br /> _Database Value:_ 'DEP' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Depreciation' |
| Purchase | Purchase value. Stored as 'PUR'. <br /> _Database Value:_ 'PUR' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Purchase' |
| Sale | Sale value. Stored as 'SLS'. <br /> _Database Value:_ 'SLS' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Sale' |
| Reevaluation | Reevaluation value. Stored as 'REV'. <br /> _Database Value:_ 'REV' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Reevaluation' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **Adjustment**  

### PositiveReserveValue

> Change in the value of the positive reserve after asset valuations (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PositiveReserveValueBase

> Change in the value of the positive reserve after asset valuations (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PurchaseValue

> Change in the purchase value of the asset (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PurchaseValueBase

> Change in the purchase value of the asset (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### SalvageValue

> Change in the salvage value of the asset (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### SalvageValueBase

> Change in the salvage value of the asset (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### Asset

> Asset for which changes in values have occurred. [Required] [Filter(multi eq)]

_Type_: **[Finance.Assets.Assets](Finance.Assets.Assets.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### AssetTransaction

> The [AssetTransaction](Finance.Assets.AssetTransactionLines.md#AssetTransaction) to which this AssetTransactionLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Assets.AssetTransactions](Finance.Assets.AssetTransactions.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ValuationModel

> Valuation model in which the changes of the asset values have occurred (Taxation model or Accounting model or other). [Required] [Filter(multi eq)]

_Type_: **[Finance.Assets.ValuationModels](Finance.Assets.ValuationModels.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Assets.AssetTransactionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.AssetTransactionLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Assets.AssetTransactionLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_AssetTransactionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_AssetTransactionLines?$top=10>

