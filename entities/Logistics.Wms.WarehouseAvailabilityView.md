---
uid: Logistics.Wms.WarehouseAvailabilityView
---
# Logistics.Wms.WarehouseAvailabilityView View

**Namespace:** [Logistics.Wms](Logistics.Wms.md)  

The availability of goods in the warehouse locations of the warehouse. Entity: Wms_Warehouse_Availability_Indexed_View (Introduced in version 21.1.1.35)

## Default Visualization
Default Display Text Format:  
_{WarehouseId}: {WarehouseLocationId}_  
Default Search Member:  
_WarehouseId_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Wms.WarehouseAvailabilityView](Logistics.Wms.WarehouseAvailabilityView.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CatchBalance](Logistics.Wms.WarehouseAvailabilityView.md#catchbalance) | decimal (nullable) | Catch (measured) quantity for the transaction. Positive values indicate transactions. Negative values are used for adjustments. null when catch measurement is not configured for the product. `Filter(eq;ge;le)` `Inherited from Wms_Warehouse_<br />Transactions_Table.Catch_Quantity` 
| [Cnt](Logistics.Wms.WarehouseAvailabilityView.md#cnt) | int64 |  
| [QuantityAvailable](Logistics.Wms.WarehouseAvailabilityView.md#quantityavailable) | decimal | The transacted net change in quantity. Positive values indicate transactions. Negative values are used for adjustments. `Required` `Default(0)` `Filter(multi eq;ge;le)` `Inherited from Wms_Warehouse_<br />Transactions_Table.Quantity` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CatchQuantityUnit](Logistics.Wms.WarehouseAvailabilityView.md#catchquantityunit) | [MeasurementUnits](General.MeasurementUnits.md) (nullable) | The measurement unit of the catch quantity. null when catch measurement is not configured for the product. `Filter(multi eq)` `Inherited from Wms_Warehouse_<br />Transactions_Table.Catch_Quantity_Unit_Id` |
| [LogisticUnit](Logistics.Wms.WarehouseAvailabilityView.md#logisticunit) | [LogisticUnits](Logistics.LogisticUnits.md) (nullable) | Logistic unit, which was transacted. null when the transaction was not for a logistic unit. `Filter(multi eq)` `Inherited from Wms_Warehouse_<br />Transactions_Table.Logistic_Unit_Id` |
| [Lot](Logistics.Wms.WarehouseAvailabilityView.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | The lot which was transacted. null when the transaction was not for a specific lot. `Filter(multi eq)` `Inherited from Wms_Warehouse_<br />Transactions_Table.Lot_Id` |
| [Product](Logistics.Wms.WarehouseAvailabilityView.md#product) | [Products](General.Products.Products.md) | The product, which was transacted. `Required` `Filter(multi eq)` `Inherited from Wms_Warehouse_<br />Transactions_Table.Product_Id` |
| [ProductVariant](Logistics.Wms.WarehouseAvailabilityView.md#productvariant) | [ProductVariants](General.ProductVariants.md) (nullable) | The product variant, which was transacted. null when the transaction was not for a product variant. `Filter(multi eq)` `Inherited from Wms_Warehouse_<br />Transactions_Table.Product_Variant_Id` |
| [QuantityUnit](Logistics.Wms.WarehouseAvailabilityView.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of quantity. `Required` `Filter(multi eq)` `Inherited from Wms_Warehouse_<br />Transactions_Table.Quantity_Unit_Id` |
| [SerialNumber](Logistics.Wms.WarehouseAvailabilityView.md#serialnumber) | [SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | The serial number which was transacted. null when the transaction was not for a specific serial number. `Filter(multi eq)` `Inherited from Wms_Warehouse_<br />Transactions_Table.Serial_Number_Id` |
| [Warehouse](Logistics.Wms.WarehouseAvailabilityView.md#warehouse) | [Warehouses](Logistics.Wms.Warehouses.md) | The warehouse in which the transaction occurred. `Required` `Filter(multi eq)` `Inherited from Wms_Warehouse_<br />Transactions_Table.Warehouse_Id` |
| [WarehouseLocation](Logistics.Wms.WarehouseAvailabilityView.md#warehouselocation) | [WarehouseLocations](Logistics.Wms.WarehouseLocations.md) | The warehouse location, where the transaction occurred. `Required` `Filter(multi eq)` `Inherited from Wms_Warehouse_<br />Transactions_Table.Warehouse_Location_Id` |


## Attribute Details

### CatchBalance

Catch (measured) quantity for the transaction. Positive values indicate transactions. Negative values are used for adjustments. null when catch measurement is not configured for the product. `Filter(eq;ge;le)` `Inherited from Wms_Warehouse_Transactions_Table.Catch_Quantity`

_Type_: **decimal (nullable)**  
_Inherited From_: **Wms_Warehouse_Transactions_Table.Catch_Quantity**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Cnt

_Type_: **int64**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### QuantityAvailable

The transacted net change in quantity. Positive values indicate transactions. Negative values are used for adjustments. `Required` `Default(0)` `Filter(multi eq;ge;le)` `Inherited from Wms_Warehouse_Transactions_Table.Quantity`

_Type_: **decimal**  
_Inherited From_: **Wms_Warehouse_Transactions_Table.Quantity**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### CatchQuantityUnit

The measurement unit of the catch quantity. null when catch measurement is not configured for the product. `Filter(multi eq)` `Inherited from Wms_Warehouse_Transactions_Table.Catch_Quantity_Unit_Id`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Inherited From_: **Wms_Warehouse_Transactions_Table.Catch_Quantity_Unit_Id**  
_Supported Filters_: **Equals, EqualsIn**  

### LogisticUnit

Logistic unit, which was transacted. null when the transaction was not for a logistic unit. `Filter(multi eq)` `Inherited from Wms_Warehouse_Transactions_Table.Logistic_Unit_Id`

_Type_: **[LogisticUnits](Logistics.LogisticUnits.md) (nullable)**  
_Inherited From_: **Wms_Warehouse_Transactions_Table.Logistic_Unit_Id**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

The lot which was transacted. null when the transaction was not for a specific lot. `Filter(multi eq)` `Inherited from Wms_Warehouse_Transactions_Table.Lot_Id`

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Inherited From_: **Wms_Warehouse_Transactions_Table.Lot_Id**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The product, which was transacted. `Required` `Filter(multi eq)` `Inherited from Wms_Warehouse_Transactions_Table.Product_Id`

_Type_: **[Products](General.Products.Products.md)**  
_Inherited From_: **Wms_Warehouse_Transactions_Table.Product_Id**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductVariant

The product variant, which was transacted. null when the transaction was not for a product variant. `Filter(multi eq)` `Inherited from Wms_Warehouse_Transactions_Table.Product_Variant_Id`

_Type_: **[ProductVariants](General.ProductVariants.md) (nullable)**  
_Inherited From_: **Wms_Warehouse_Transactions_Table.Product_Variant_Id**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

The measurement unit of quantity. `Required` `Filter(multi eq)` `Inherited from Wms_Warehouse_Transactions_Table.Quantity_Unit_Id`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Inherited From_: **Wms_Warehouse_Transactions_Table.Quantity_Unit_Id**  
_Supported Filters_: **Equals, EqualsIn**  

### SerialNumber

The serial number which was transacted. null when the transaction was not for a specific serial number. `Filter(multi eq)` `Inherited from Wms_Warehouse_Transactions_Table.Serial_Number_Id`

_Type_: **[SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Inherited From_: **Wms_Warehouse_Transactions_Table.Serial_Number_Id**  
_Supported Filters_: **Equals, EqualsIn**  

### Warehouse

The warehouse in which the transaction occurred. `Required` `Filter(multi eq)` `Inherited from Wms_Warehouse_Transactions_Table.Warehouse_Id`

_Type_: **[Warehouses](Logistics.Wms.Warehouses.md)**  
_Inherited From_: **Wms_Warehouse_Transactions_Table.Warehouse_Id**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseLocation

The warehouse location, where the transaction occurred. `Required` `Filter(multi eq)` `Inherited from Wms_Warehouse_Transactions_Table.Warehouse_Location_Id`

_Type_: **[WarehouseLocations](Logistics.Wms.WarehouseLocations.md)**  
_Inherited From_: **Wms_Warehouse_Transactions_Table.Warehouse_Location_Id**  
_Supported Filters_: **Equals, EqualsIn**  


## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseAvailabilityView?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseAvailabilityView?$top=10>

