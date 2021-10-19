---
uid: Applications.AssetManagement.MaintenanceOrderLines
---
# Applications.AssetManagement.MaintenanceOrderLines Entity

**Namespace:** [Applications.AssetManagement](Applications.AssetManagement.md)  

Contains the types of maintenance and maintained assets in the maintenance orders. Entity: Eam_Maintenance_Order_Lines (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{LineNo}. {MaintenanceOrder.DocumentNo} {MaintenanceOrder.DocumentType.TypeName:T}_  
Default Search Member:  
_MaintenanceOrder.DocumentNo_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.AssetManagement.MaintenanceOrders](Applications.AssetManagement.MaintenanceOrders.md)  
Aggregate Root:  
[Applications.AssetManagement.MaintenanceOrders](Applications.AssetManagement.MaintenanceOrders.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.AssetManagement.MaintenanceOrderLines.md#id) | guid |  
| [LineNo](Applications.AssetManagement.MaintenanceOrderLines.md#lineno) | int32 | Consecutive line number, unique within the maintenance order. `Required` 
| [NextServiceDate](Applications.AssetManagement.MaintenanceOrderLines.md#nextservicedate) | date __nullable__ | Specifies, that the maintenance required a specific date for the next maintenance. null means that default scheduling should be used. 
| [NextServiceTracked<br />ParameterValue](Applications.AssetManagement.MaintenanceOrderLines.md#nextservicetrackedparametervalue) | int32 __nullable__ | Specifies, that the maintenance required the next maintenance to be performed on a specific value of the tracked parameter. null means that default scheduling should be used. 
| [Notes](Applications.AssetManagement.MaintenanceOrderLines.md#notes) | string (max) __nullable__ | Notes for this MaintenanceOrderLine. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Applications.AssetManagement.MaintenanceOrderLines.md#document) | [MaintenanceOrders](Applications.AssetManagement.MaintenanceOrders.md) | The `MaintenanceOrder`(Applications.AssetManagement.MaintenanceOrderLines.md#maintenanceorder) to which this MaintenanceOrderLine belongs. `Required` `Filter(multi eq)` |
| [MaintenanceOrder](Applications.AssetManagement.MaintenanceOrderLines.md#maintenanceorder) | [MaintenanceOrders](Applications.AssetManagement.MaintenanceOrders.md) | The `MaintenanceOrder`(Applications.AssetManagement.MaintenanceOrderLines.md#maintenanceorder) to which this MaintenanceOrderLine belongs. `Required` `Filter(multi eq)` `Owner` |
| [MaintenanceType](Applications.AssetManagement.MaintenanceOrderLines.md#maintenancetype) | [MaintenanceTypes](Applications.AssetManagement.MaintenanceTypes.md) | The type of maintenance performed. `Required` `Filter(multi eq)` |
| [ManagedAsset](Applications.AssetManagement.MaintenanceOrderLines.md#managedasset) | [ManagedAssets](Applications.AssetManagement.ManagedAssets.md) | The maintained asset. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive line number, unique within the maintenance order. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.MaintenanceOrder.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.MaintenanceOrder.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### NextServiceDate

Specifies, that the maintenance required a specific date for the next maintenance. null means that default scheduling should be used.

_Type_: **date __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### NextServiceTrackedParameterValue

Specifies, that the maintenance required the next maintenance to be performed on a specific value of the tracked parameter. null means that default scheduling should be used.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

Notes for this MaintenanceOrderLine.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### Document

The `MaintenanceOrder`(Applications.AssetManagement.MaintenanceOrderLines.md#maintenanceorder) to which this MaintenanceOrderLine belongs. `Required` `Filter(multi eq)`

_Type_: **[MaintenanceOrders](Applications.AssetManagement.MaintenanceOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### MaintenanceOrder

The `MaintenanceOrder`(Applications.AssetManagement.MaintenanceOrderLines.md#maintenanceorder) to which this MaintenanceOrderLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[MaintenanceOrders](Applications.AssetManagement.MaintenanceOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### MaintenanceType

The type of maintenance performed. `Required` `Filter(multi eq)`

_Type_: **[MaintenanceTypes](Applications.AssetManagement.MaintenanceTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ManagedAsset

The maintained asset. `Required` `Filter(multi eq)`

_Type_: **[ManagedAssets](Applications.AssetManagement.ManagedAssets.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Applications.AssetManagement.MaintenanceOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.AssetManagement.MaintenanceOrderLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_MaintenanceOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_MaintenanceOrderLines?$top=10>

