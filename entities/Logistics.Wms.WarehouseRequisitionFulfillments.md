---
uid: Logistics.Wms.WarehouseRequisitionFulfillments
---
# Logistics.Wms.WarehouseRequisitionFulfillments Entity

**Namespace:** [Logistics.Wms](Logistics.Wms.md)  

Fulfillment ledger for warehouse requisitions. Entity: Wms_Warehouse_Requisition_Fulfillments (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Id}: {WarehouseRequisitionId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Wms.WarehouseRequisitionFulfillments](Logistics.Wms.WarehouseRequisitionFulfillments.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationTimeUtc](Logistics.Wms.WarehouseRequisitionFulfillments.md#creationtimeutc) | datetime | The exact time in UTC, when the fulfillment was created in the system. `Required` 
| [FulfillmentType](Logistics.Wms.WarehouseRequisitionFulfillments.md#fulfillmenttype) | string (1) | Type of fulfillment: P=Plan created; C=Requisition completed. `Required` 
| [Id](Logistics.Wms.WarehouseRequisitionFulfillments.md#id) | guid |  
| [IsFinal](Logistics.Wms.WarehouseRequisitionFulfillments.md#isfinal) | boolean | Specifies whether this fulfillment finalizes the requisition line, regardless of any remaining quantities. `Required` 
| [Quantity](Logistics.Wms.WarehouseRequisitionFulfillments.md#quantity) | decimal (12, 3) | Quantity fulfilled (in the measurement unit of the requisition line). `Required` 
| [RowVersion](Logistics.Wms.WarehouseRequisitionFulfillments.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationUser](Logistics.Wms.WarehouseRequisitionFulfillments.md#creationuser) | [Users](Systems.Security.Users.md) | The user, who created the record. `Required` `Filter(multi eq)` |
| [WarehouseRequisition](Logistics.Wms.WarehouseRequisitionFulfillments.md#warehouserequisition) | [WarehouseRequisitions](Logistics.Wms.WarehouseRequisitions.md) | The warehouse requisiton, which is fulfilled. `Required` `Filter(multi eq)` |
| [WarehouseRequisitionLine](Logistics.Wms.WarehouseRequisitionFulfillments.md#warehouserequisitionline) | [WarehouseRequisitionLines](Logistics.Wms.WarehouseRequisitionLines.md) | The requisition line, which is fulfilled. `Required` `Filter(multi eq)` |


## Attribute Details

### CreationTimeUtc

The exact time in UTC, when the fulfillment was created in the system. `Required`

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FulfillmentType

Type of fulfillment: P=Plan created; C=Requisition completed. `Required`

_Type_: **string (1)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **1**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsFinal

Specifies whether this fulfillment finalizes the requisition line, regardless of any remaining quantities. `Required`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Quantity

Quantity fulfilled (in the measurement unit of the requisition line). `Required`

_Type_: **decimal (12, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CreationUser

The user, who created the record. `Required` `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseRequisition

The warehouse requisiton, which is fulfilled. `Required` `Filter(multi eq)`

_Type_: **[WarehouseRequisitions](Logistics.Wms.WarehouseRequisitions.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseRequisitionLine

The requisition line, which is fulfilled. `Required` `Filter(multi eq)`

_Type_: **[WarehouseRequisitionLines](Logistics.Wms.WarehouseRequisitionLines.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Logistics.Wms.WarehouseRequisitionFulfillments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Wms.WarehouseRequisitionFulfillments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseRequisitionFulfillments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseRequisitionFulfillments?$top=10>

