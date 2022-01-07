---
uid: Logistics.Wms.Warehouses
---
# Logistics.Wms.Warehouses Entity

**Namespace:** [Logistics.Wms](Logistics.Wms.md)  

Physical warehouse. Entity: Wms_Warehouses (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Name_  
Name Data Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md)  
  * [Logistics.Wms.WarehouseLocations](Logistics.Wms.WarehouseLocations.md)  
  * [Logistics.Wms.WarehouseWorkers](Logistics.Wms.WarehouseWorkers.md)  
  * [Logistics.Wms.WarehouseZones](Logistics.Wms.WarehouseZones.md)  
  * [Logistics.Wms.WarehousePolicies](Logistics.Wms.WarehousePolicies.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](Logistics.Wms.Warehouses.md#displaytext) | string |  
| [Id](Logistics.Wms.Warehouses.md#id) | guid |  
| [Name](Logistics.Wms.Warehouses.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the warehouse (multilanguage). `Required` `Filter(eq;like)` 
| [Notes](Logistics.Wms.Warehouses.md#notes) | string (max) __nullable__ | Notes for this Warehouse. 
| [ObjectVersion](Logistics.Wms.Warehouses.md#objectversion) | int32 |  

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Locations | [WarehouseLocations](Logistics.Wms.WarehouseLocations.md) | List of `WarehouseLocation`(Logistics.Wms.WarehouseLocations.md) child objects, based on the `Logistics.Wms.WarehouseLocation.Warehouse`(Logistics.Wms.WarehouseLocations.md#warehouse) back reference 
| Policies | [WarehousePolicies](Logistics.Wms.WarehousePolicies.md) | List of `WarehousePolicy`(Logistics.Wms.WarehousePolicies.md) child objects, based on the `Logistics.Wms.WarehousePolicy.Warehouse`(Logistics.Wms.WarehousePolicies.md#warehouse) back reference 
| Workers | [WarehouseWorkers](Logistics.Wms.WarehouseWorkers.md) | List of `WarehouseWorker`(Logistics.Wms.WarehouseWorkers.md) child objects, based on the `Logistics.Wms.WarehouseWorker.Warehouse`(Logistics.Wms.WarehouseWorkers.md#warehouse) back reference 
| Zones | [WarehouseZones](Logistics.Wms.WarehouseZones.md) | List of `WarehouseZone`(Logistics.Wms.WarehouseZones.md) child objects, based on the `Logistics.Wms.WarehouseZone.Warehouse`(Logistics.Wms.WarehouseZones.md#warehouse) back reference 


## Attribute Details

### DisplayText

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the warehouse (multilanguage). `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this Warehouse.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Logistics.Wms.Warehouses erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Wms.Warehouses erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_Warehouses?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_Warehouses?$top=10>

