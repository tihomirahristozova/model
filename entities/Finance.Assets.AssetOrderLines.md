---
uid: Finance.Assets.AssetOrderLines
---
# Finance.Assets.AssetOrderLines

Asset purchase or sales order line for one asset. Entity: Ast_Asset_Order_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Assets.AssetOrderLines.md#Id) | guid |  
| [AssetValue](Finance.Assets.AssetOrderLines.md#AssetValue) | [Amount](../data-types.md#Amount) | Value of the acquired or retired asset. [Currency: AssetValueCurrency] [Required] [Default(0)] 
| [ParentLineNo](Finance.Assets.AssetOrderLines.md#ParentLineNo) | int32 (nullable) | The number of the line within the parent document, which the current line executes. null when the current line does not execute line. (Introduced in version 18.2.100.0) 
| [Quantity](Finance.Assets.AssetOrderLines.md#Quantity) | int32 | Indicates the nature of the current operation: 1 - the operation is applied, 0 - no change, -1 - the operation is cancelled. [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Asset](Finance.Assets.AssetOrderLines.md#Asset) | [Finance.Assets.Assets](Finance.Assets.Assets.md) | The asset that is acquired or retired. [Required] [Filter(multi eq)] |
| [AssetOrder](Finance.Assets.AssetOrderLines.md#AssetOrder) | [Finance.Assets.AssetOrders](Finance.Assets.AssetOrders.md) | The [AssetOrder](Finance.Assets.AssetOrderLines.md#AssetOrder) to which this AssetOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [AssetValueCurrency](Finance.Assets.AssetOrderLines.md#AssetValueCurrency) | [General.Currencies](General.Currencies.md) | Currency of Asset Value. [Required] [Filter(multi eq)] |
| [ParentDocument](Finance.Assets.AssetOrderLines.md#ParentDocument) | [General.Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] (Introduced in version 18.2.100.0) |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AssetValue

> Value of the acquired or retired asset. [Currency: AssetValueCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ParentLineNo

> The number of the line within the parent document, which the current line executes. null when the current line does not execute line. (Introduced in version 18.2.100.0)

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Quantity

> Indicates the nature of the current operation: 1 - the operation is applied, 0 - no change, -1 - the operation is cancelled. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### Asset

> The asset that is acquired or retired. [Required] [Filter(multi eq)]

_Type_: **[Finance.Assets.Assets](Finance.Assets.Assets.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### AssetOrder

> The [AssetOrder](Finance.Assets.AssetOrderLines.md#AssetOrder) to which this AssetOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Assets.AssetOrders](Finance.Assets.AssetOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### AssetValueCurrency

> Currency of Asset Value. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ParentDocument

> The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] (Introduced in version 18.2.100.0)

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Assets.AssetOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.AssetOrderLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Assets.AssetOrderLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_AssetOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_AssetOrderLines?$top=10>

