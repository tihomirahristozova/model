---
uid: Logistics.Wms.WarehouseTransactions
---
# Logistics.Wms.WarehouseTransactions Entity

**Namespace:** [Logistics.Wms](Logistics.Wms.md)  

Represents increase or decrease in the quantity available in a warehouse location. Entity: Wms_Warehouse_Transactions (Introduced in version 21.1.1.26)

## Default Visualization
Default Display Text Format:  
_{Id}_  
Default Search Member:  
_Id_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Wms.WarehouseTransactions](Logistics.Wms.WarehouseTransactions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CatchQuantity](Logistics.Wms.WarehouseTransactions.md#catchquantity) | decimal (nullable) | Catch (measured) quantity for the transaction. Positive values indicate transactions. Negative values are used for adjustments. null when catch measurement is not configured for the product. `Filter(eq;ge;le)` 
| [CreationTimeUtc](Logistics.Wms.WarehouseTransactions.md#creationtimeutc) | datetime |  
| [Direction](Logistics.Wms.WarehouseTransactions.md#direction) | [Direction](Logistics.Wms.WarehouseTransactions.md#direction) | Direction of the transaction - I=IN, O=OUT. `Required` `Default("I")` `Filter(eq)` 
| [Id](Logistics.Wms.WarehouseTransactions.md#id) | guid |  
| [Quantity](Logistics.Wms.WarehouseTransactions.md#quantity) | decimal | The transacted net change in quantity. Positive values indicate transactions. Negative values are used for adjustments. `Required` `Default(0)` `Filter(multi eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CatchQuantityUnit](Logistics.Wms.WarehouseTransactions.md#catchquantityunit) | [MeasurementUnits](General.MeasurementUnits.md) (nullable) | The measurement unit of the catch quantity. null when catch measurement is not configured for the product. `Filter(multi eq)` |
| [CreationUser](Logistics.Wms.WarehouseTransactions.md#creationuser) | [Users](Systems.Security.Users.md) |  |
| [LogisticUnit](Logistics.Wms.WarehouseTransactions.md#logisticunit) | [LogisticUnits](Logistics.LogisticUnits.md) (nullable) | Logistic unit, which was transacted. null when the transaction was not for a logistic unit. `Filter(multi eq)` |
| [Lot](Logistics.Wms.WarehouseTransactions.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | The lot which was transacted. null when the transaction was not for a specific lot. `Filter(multi eq)` |
| [Product](Logistics.Wms.WarehouseTransactions.md#product) | [Products](General.Products.Products.md) | The product, which was transacted. `Required` `Filter(multi eq)` |
| [ProductVariant](Logistics.Wms.WarehouseTransactions.md#productvariant) | [ProductVariants](General.ProductVariants.md) (nullable) | The product variant, which was transacted. null when the transaction was not for a product variant. `Filter(multi eq)` |
| [QuantityUnit](Logistics.Wms.WarehouseTransactions.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of quantity. `Required` `Filter(multi eq)` |
| [SerialNumber](Logistics.Wms.WarehouseTransactions.md#serialnumber) | [SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | The serial number which was transacted. null when the transaction was not for a specific serial number. `Filter(multi eq)` |
| [Warehouse](Logistics.Wms.WarehouseTransactions.md#warehouse) | [Warehouses](Logistics.Wms.Warehouses.md) | The warehouse in which the transaction occurred. `Required` `Filter(multi eq)` |
| [WarehouseLocation](Logistics.Wms.WarehouseTransactions.md#warehouselocation) | [WarehouseLocations](Logistics.Wms.WarehouseLocations.md) | The warehouse location, where the transaction occurred. `Required` `Filter(multi eq)` |
| [WarehouseOrder](Logistics.Wms.WarehouseTransactions.md#warehouseorder) | [WarehouseOrders](Logistics.Wms.WarehouseOrders.md) (nullable) | The order which created this transaction. null when this transaction was not based on order. `Filter(multi eq)` |
| [WarehouseOrderLine](Logistics.Wms.WarehouseTransactions.md#warehouseorderline) | [WarehouseOrderLines](Logistics.Wms.WarehouseOrderLines.md) (nullable) | The order line which created this transaction. null when this transaction was not based on order line. `Filter(multi eq)` |


## Attribute Details

### CatchQuantity

Catch (measured) quantity for the transaction. Positive values indicate transactions. Negative values are used for adjustments. null when catch measurement is not configured for the product. `Filter(eq;ge;le)`

_Type_: **decimal (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CreationTimeUtc

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTimeUtc**  

### Direction

Direction of the transaction - I=IN, O=OUT. `Required` `Default("I")` `Filter(eq)`

_Type_: **[Direction](Logistics.Wms.WarehouseTransactions.md#direction)**  
Allowed values for the `Direction`(Logistics.Wms.WarehouseTransactions.md#direction) data attribute  
_Allowed Values (Logistics.Wms.WarehouseTransactionsRepository.Direction Enum Members)_  

| Value | Description |
| ---- | --- |
| IN | IN value. Stored as 'I'. <br /> _Database Value:_ 'I' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'IN' |
| OUT | OUT value. Stored as 'O'. <br /> _Database Value:_ 'O' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'OUT' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **IN**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Quantity

The transacted net change in quantity. Positive values indicate transactions. Negative values are used for adjustments. `Required` `Default(0)` `Filter(multi eq;ge;le)`

_Type_: **decimal**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### CatchQuantityUnit

The measurement unit of the catch quantity. null when catch measurement is not configured for the product. `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CreationUser

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### LogisticUnit

Logistic unit, which was transacted. null when the transaction was not for a logistic unit. `Filter(multi eq)`

_Type_: **[LogisticUnits](Logistics.LogisticUnits.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

The lot which was transacted. null when the transaction was not for a specific lot. `Filter(multi eq)`

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The product, which was transacted. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductVariant

The product variant, which was transacted. null when the transaction was not for a product variant. `Filter(multi eq)`

_Type_: **[ProductVariants](General.ProductVariants.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

The measurement unit of quantity. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### SerialNumber

The serial number which was transacted. null when the transaction was not for a specific serial number. `Filter(multi eq)`

_Type_: **[SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Warehouse

The warehouse in which the transaction occurred. `Required` `Filter(multi eq)`

_Type_: **[Warehouses](Logistics.Wms.Warehouses.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseLocation

The warehouse location, where the transaction occurred. `Required` `Filter(multi eq)`

_Type_: **[WarehouseLocations](Logistics.Wms.WarehouseLocations.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseOrder

The order which created this transaction. null when this transaction was not based on order. `Filter(multi eq)`

_Type_: **[WarehouseOrders](Logistics.Wms.WarehouseOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseOrderLine

The order line which created this transaction. null when this transaction was not based on order line. `Filter(multi eq)`

_Type_: **[WarehouseOrderLines](Logistics.Wms.WarehouseOrderLines.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Wms.WarehouseTransactions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Wms.WarehouseTransactions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseTransactions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseTransactions?$top=10>

