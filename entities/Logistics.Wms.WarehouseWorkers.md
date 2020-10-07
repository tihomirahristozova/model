# Logistics.Wms.WarehouseWorkers

Human or robot worker, which can execute warehouse tasks. Entity: Wms_Warehouse_Workers (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Wms.WarehouseWorkers.md#Id) | guid |  
| [ActiveFrom](Logistics.Wms.WarehouseWorkers.md#ActiveFrom) | date | The date, from which the worker record has become active in the warehouse. [Required] [Default(Today)] [Filter(eq;ge;le)] 
| [ActiveTo](Logistics.Wms.WarehouseWorkers.md#ActiveTo) | date (nullable) | The date of termination of the activity of the worker in the warehouse. Can be null for workers, which are still active and do not have previous terminations. [Filter(eq;ge;le)] 
| [IsActive](Logistics.Wms.WarehouseWorkers.md#IsActive) | boolean | Specifies whether the worker is active and can execute new warehouse tasks. [Required] [Default(true)] [Filter(eq)] 
| [Notes](Logistics.Wms.WarehouseWorkers.md#Notes) | string (nullable) | Notes for this WarehouseWorker. 
| [Name](Logistics.Wms.WarehouseWorkers.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | Name of the worker (multi-language). [Required] [Filter(multi eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Person](Logistics.Wms.WarehouseWorkers.md#Person) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | The definition of the person, when the worker is human worker. null means that the person is unknown or the worker is non-person. [Filter(multi eq)] |
| [Warehouse](Logistics.Wms.WarehouseWorkers.md#Warehouse) | [Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md) | The warehouse, where the worker works. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ActiveFrom

> The date, from which the worker record has become active in the warehouse. [Required] [Default(Today)] [Filter(eq;ge;le)]

_Type_: **date**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### ActiveTo

> The date of termination of the activity of the worker in the warehouse. Can be null for workers, which are still active and do not have previous terminations. [Filter(eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### IsActive

> Specifies whether the worker is active and can execute new warehouse tasks. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

> Notes for this WarehouseWorker.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> Name of the worker (multi-language). [Required] [Filter(multi eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### Person

> The definition of the person, when the worker is human worker. null means that the person is unknown or the worker is non-person. [Filter(multi eq)]

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Warehouse

> The warehouse, where the worker works. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Wms.WarehouseWorkers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Wms.WarehouseWorkers erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Wms.WarehouseWorkers erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseWorkers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseWorkers?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Wms_Warehouse_Workers?$top=10>

