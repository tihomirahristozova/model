# Logistics.Inventory.ReconciliationOrderLines

Obsolete. Not used. Entity: Inv_Reconciliation_Order_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.ReconciliationOrderLines.md#Id) | guid |  
| [LineNo](Logistics.Inventory.ReconciliationOrderLines.md#LineNo) | int32 | Line number within the reconciliation order. [Required] [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Product](Logistics.Inventory.ReconciliationOrderLines.md#Product) | [General.Products.Products](General.Products.Products.md) | The item which quantity should be reconciled. [Required] [Filter(multi eq)] |
| [ReconciliationOrder](Logistics.Inventory.ReconciliationOrderLines.md#ReconciliationOrder) | [Logistics.Inventory.ReconciliationOrders](Logistics.Inventory.ReconciliationOrders.md) | Reconciliation order header. [Required] [Filter(multi eq)] [Owner] |
| [SerialNumber](Logistics.Inventory.ReconciliationOrderLines.md#SerialNumber) | [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Serial number of the product, which should be reconciled. [Filter(multi eq)] |
| [StoreBin](Logistics.Inventory.ReconciliationOrderLines.md#StoreBin) | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | Specifies store bin, that should be reconciled. null means to reconcile all or any bin. [Filter(multi eq)] |
| [Store](Logistics.Inventory.ReconciliationOrderLines.md#Store) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) | Store, which should be checked. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### LineNo

> Line number within the reconciliation order. [Required] [Filter(eq;ge;le)]

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.ReconciliationOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.ReconciliationOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

## Reference Details

### Product

> The item which quantity should be reconciled. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ReconciliationOrder

> Reconciliation order header. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Inventory.ReconciliationOrders](Logistics.Inventory.ReconciliationOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SerialNumber

> Serial number of the product, which should be reconciled. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### StoreBin

> Specifies store bin, that should be reconciled. null means to reconcile all or any bin. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Store

> Store, which should be checked. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.ReconciliationOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.ReconciliationOrderLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.ReconciliationOrderLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_ReconciliationOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_ReconciliationOrderLines?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Inv_Reconciliation_Order_Lines?$top=10>

