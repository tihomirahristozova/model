---
uid: Finance.Assets.AssetOrderLines
---
# Finance.Assets.AssetOrderLines Entity

**Namespace:** [Finance.Assets](Finance.Assets.md)  

Asset purchase or sales order line for one asset. Entity: Ast_Asset_Order_Lines

## Default Visualization
Default Display Text Format:  
_{AssetOrder.EntityName}_  
Default Search Members:  
_AssetOrder.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Assets.AssetOrders](Finance.Assets.AssetOrders.md)  
Aggregate Root:  
[Finance.Assets.AssetOrders](Finance.Assets.AssetOrders.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AssetValue](Finance.Assets.AssetOrderLines.md#assetvalue) | [Amount (14, 2)](../data-types.md#amount) | Value of the acquired or retired asset. `Currency: AssetValueCurrency` `Required` `Default(0)` 
| [Id](Finance.Assets.AssetOrderLines.md#id) | guid |  
| [ObjectVersion](Finance.Assets.AssetOrderLines.md#objectversion) | int32 |  
| [ParentLineNo](Finance.Assets.AssetOrderLines.md#parentlineno) | int32 __nullable__ | The number of the line within the parent document, which the current line executes. null when the current line does not execute line. `Introduced in version 18.2` 
| [Quantity](Finance.Assets.AssetOrderLines.md#quantity) | int32 | Indicates the nature of the current operation: 1 - the operation is applied, 0 - no change, -1 - the operation is cancelled. `Required` `Default(0)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Asset](Finance.Assets.AssetOrderLines.md#asset) | [Assets](Finance.Assets.Assets.md) | The asset that is acquired or retired. `Required` `Filter(multi eq)` |
| [AssetOrder](Finance.Assets.AssetOrderLines.md#assetorder) | [AssetOrders](Finance.Assets.AssetOrders.md) | The <see cref="AssetOrder"/> to which this AssetOrderLine belongs. `Required` `Filter(multi eq)` `Owner` |
| [AssetValueCurrency](Finance.Assets.AssetOrderLines.md#assetvaluecurrency) | [Currencies](General.Currencies.md) | Currency of Asset Value. `Required` `Filter(multi eq)` |
| [Document](Finance.Assets.AssetOrderLines.md#document) | [AssetOrders](Finance.Assets.AssetOrders.md) | The <see cref="AssetOrder"/> to which this AssetOrderLine belongs. `Required` `Filter(multi eq)` |
| [ParentDocument](Finance.Assets.AssetOrderLines.md#parentdocument) | [Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. `Filter(multi eq)` `Introduced in version 18.2` |


## Attribute Details

### AssetValue

Value of the acquired or retired asset. `Currency: AssetValueCurrency` `Required` `Default(0)`

_Type_: **[Amount (14, 2)](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ParentLineNo

The number of the line within the parent document, which the current line executes. null when the current line does not execute line. `Introduced in version 18.2`

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Quantity

Indicates the nature of the current operation: 1 - the operation is applied, 0 - no change, -1 - the operation is cancelled. `Required` `Default(0)`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### Asset

The asset that is acquired or retired. `Required` `Filter(multi eq)`

_Type_: **[Assets](Finance.Assets.Assets.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### AssetOrder

The <see cref="AssetOrder"/> to which this AssetOrderLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[AssetOrders](Finance.Assets.AssetOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### AssetValueCurrency

Currency of Asset Value. `Required` `Filter(multi eq)`

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Document

The <see cref="AssetOrder"/> to which this AssetOrderLine belongs. `Required` `Filter(multi eq)`

_Type_: **[AssetOrders](Finance.Assets.AssetOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ParentDocument

The document, which the current line executes. null when the current line does not execute another line. `Filter(multi eq)` `Introduced in version 18.2`

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Assets.AssetOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Assets.AssetOrderLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_AssetOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_AssetOrderLines?$top=10>

