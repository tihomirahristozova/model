---
uid: Logistics.Inventory.ReconciliationLines
---
# Logistics.Inventory.ReconciliationLines Entity

**Namespace:** [Logistics.Inventory](Logistics.Inventory.md)  

Store reconciliations (physical counting) detail lines. Each line contains the reconciliation for one combination of product, lot, bin and serial number. Entity: Inv_Reconciliation_Lines

## Default Visualization
Default Display Text Format:  
_{LineOrd}. {Reconciliation.DocumentNo} {Reconciliation.DocumentType.TypeName:T}_  
Default Search Members:  
_Reconciliation.DocumentNo_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Inventory.Reconciliations](Logistics.Inventory.Reconciliations.md)  
Aggregate Root:  
[Logistics.Inventory.Reconciliations](Logistics.Inventory.Reconciliations.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AvailableQuantityBase](Logistics.Inventory.ReconciliationLines.md#availablequantitybase) | [Quantity (18, 3)](../data-types.md#quantity) | Quantity found at the reconciliation, in the base measurement category of the product. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `ReadOnly` 
| [Id](Logistics.Inventory.ReconciliationLines.md#id) | guid |  
| [LineOrd](Logistics.Inventory.ReconciliationLines.md#lineord) | int32 | The ordinal position of the line within the document. Duplicates are allowed, but not suggested. `Required` 
| [Notes](Logistics.Inventory.ReconciliationLines.md#notes) | string (254) __nullable__ | Notes for this ReconciliationLine. 
| [ObjectVersion](Logistics.Inventory.ReconciliationLines.md#objectversion) | int32 |  
| [Quantity](Logistics.Inventory.ReconciliationLines.md#quantity) | [Quantity (18, 3)](../data-types.md#quantity) | Quantity found at the reconciliation, . `Unit: QuantityUnit` `Required` `Filter(ge;le)` 
| [QuantityBase](Logistics.Inventory.ReconciliationLines.md#quantitybase) | [Quantity (18, 3)](../data-types.md#quantity) | Quantity found at the reconciliation, expressed in base measurement units. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Filter(ge;le)` 
| [StandardQuantityBase](Logistics.Inventory.ReconciliationLines.md#standardquantitybase) | [Quantity (18, 3)](../data-types.md#quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `ReadOnly` `Introduced in version 18.2` 
| [TransactionTimestamp](Logistics.Inventory.ReconciliationLines.md#transactiontimestamp) | datetime __nullable__ | Exact time when the transaction occurred. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Logistics.Inventory.ReconciliationLines.md#document) | [Reconciliations](Logistics.Inventory.Reconciliations.md) | Parent reconciliation Id. `Required` `Filter(multi eq)` |
| [Lot](Logistics.Inventory.ReconciliationLines.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | The lot, which was reconciled. `Filter(multi eq)` |
| [Product](Logistics.Inventory.ReconciliationLines.md#product) | [Products](General.Products.Products.md) | The id of the reconciled product. `Required` `Filter(multi eq)` |
| [ProductCode](Logistics.Inventory.ReconciliationLines.md#productcode) | [ProductCodes](General.Products.ProductCodes.md) (nullable) | Selects the product thru some of the product codes. `Filter(multi eq)` |
| [QuantityUnit](Logistics.Inventory.ReconciliationLines.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. `Required` `Filter(multi eq)` |
| [Reconciliation](Logistics.Inventory.ReconciliationLines.md#reconciliation) | [Reconciliations](Logistics.Inventory.Reconciliations.md) | Parent reconciliation Id. `Required` `Filter(multi eq)` `Owner` |
| [SerialNumber](Logistics.Inventory.ReconciliationLines.md#serialnumber) | [SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Item serial number for serialized items. null for non-serializable items. `Filter(multi eq)` |
| [Store](Logistics.Inventory.ReconciliationLines.md#store) | [Stores](Logistics.Inventory.Stores.md) | The store, containing the reconciled product. `Required` `Filter(multi eq)` |
| [StoreBin](Logistics.Inventory.ReconciliationLines.md#storebin) | [StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | The store bin, that was counted. `Filter(multi eq)` |


## Attribute Details

### AvailableQuantityBase

Quantity found at the reconciliation, in the base measurement category of the product. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `ReadOnly`

_Type_: **[Quantity (18, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineOrd

The ordinal position of the line within the document. Duplicates are allowed, but not suggested. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.Reconciliation.Lines.Select( c => c.LineOrd).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.Reconciliation.Lines.Select( c => c.LineOrd).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this ReconciliationLine.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Quantity

Quantity found at the reconciliation, . `Unit: QuantityUnit` `Required` `Filter(ge;le)`

_Type_: **[Quantity (18, 3)](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### QuantityBase

Quantity found at the reconciliation, expressed in base measurement units. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Filter(ge;le)`

_Type_: **[Quantity (18, 3)](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### StandardQuantityBase

The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `ReadOnly` `Introduced in version 18.2`

_Type_: **[Quantity (18, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### TransactionTimestamp

Exact time when the transaction occurred.

_Type_: **datetime __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Document

Parent reconciliation Id. `Required` `Filter(multi eq)`

_Type_: **[Reconciliations](Logistics.Inventory.Reconciliations.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

The lot, which was reconciled. `Filter(multi eq)`

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The id of the reconciled product. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.ProductCode.Product.IfNullThen( obj.Product)`
### ProductCode

Selects the product thru some of the product codes. `Filter(multi eq)`

_Type_: **[ProductCodes](General.Products.ProductCodes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Product != null) AndAlso ( obj.ProductCode != null)) AndAlso ( obj.Product != obj.ProductCode.Product)), null, obj.ProductCode)`
### QuantityUnit

The measurement unit of Quantity. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.ProductCode.CodingSystem.DefaultMeasurementUnit.IfNullThen( obj.Product.MeasurementUnit.IfNullThen( obj.QuantityUnit))`
### Reconciliation

Parent reconciliation Id. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Reconciliations](Logistics.Inventory.Reconciliations.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### SerialNumber

Item serial number for serialized items. null for non-serializable items. `Filter(multi eq)`

_Type_: **[SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

The store, containing the reconciled product. `Required` `Filter(multi eq)`

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Reconciliation.DefaultStore.IfNullThen( obj.Store)`
### StoreBin

The store bin, that was counted. `Filter(multi eq)`

_Type_: **[StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Reconciliation.DefaultStoreBin.IfNullThen( obj.StoreBin)`


## Business Rules

[!list limit=1000 erp.entity=Logistics.Inventory.ReconciliationLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Inventory.ReconciliationLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_ReconciliationLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_ReconciliationLines?$top=10>

