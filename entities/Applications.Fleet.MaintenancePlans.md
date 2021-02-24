---
uid: Applications.Fleet.MaintenancePlans
---
# Applications.Fleet.MaintenancePlans Entity

**Namespace:** [Applications.Fleet](Applications.Fleet.md)  

Defines the periodic maintenance plans and the conditions for performing the next maintenance. Entity: Fleet_Maintenance_Plans

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
  @aggregates  
Aggregate Tree  
* [Applications.Fleet.MaintenancePlans](Applications.Fleet.MaintenancePlans.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CheckDays](Applications.Fleet.MaintenancePlans.md#checkdays) | int32 (nullable) | When not null, specifies the number of days between maintenances. 
| [CheckMonths](Applications.Fleet.MaintenancePlans.md#checkmonths) | int32 (nullable) | When not null, specifies the number of months between maintenances. 
| [Code](Applications.Fleet.MaintenancePlans.md#code) | string | The unique code of the MaintenancePlan. [Required] 
| [Id](Applications.Fleet.MaintenancePlans.md#id) | guid |  
| [IsActive](Applications.Fleet.MaintenancePlans.md#isactive) | boolean | True if the plan is active and can be selected from drop-downs. [Required] [Default(true)] [Introduced in version 18.2] 
| [MileageKm](Applications.Fleet.MaintenancePlans.md#mileagekm) | int32 (nullable) | When not null, specifies the number of kilometers that must have passed since the last maintenance, for the next maintenance to occur. 
| [Name](Applications.Fleet.MaintenancePlans.md#name) | string | Maintenance plan name (Multilanguage). [Required] 
| [Notes](Applications.Fleet.MaintenancePlans.md#notes) | string (nullable) | Notes for this MaintenancePlan. 
| [TripCount](Applications.Fleet.MaintenancePlans.md#tripcount) | int32 (nullable) | When not null, specifies the number of trips that must be performed since the last maintenance, for the next maintenance to occur. 


## Attribute Details

### CheckDays

When not null, specifies the number of days between maintenances.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CheckMonths

When not null, specifies the number of months between maintenances.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Code

The unique code of the MaintenancePlan. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

True if the plan is active and can be selected from drop-downs. [Required] [Default(true)] [Introduced in version 18.2]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### MileageKm

When not null, specifies the number of kilometers that must have passed since the last maintenance, for the next maintenance to occur.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

Maintenance plan name (Multilanguage). [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

Notes for this MaintenancePlan.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TripCount

When not null, specifies the number of trips that must be performed since the last maintenance, for the next maintenance to occur.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Fleet.MaintenancePlans erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.MaintenancePlans erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_MaintenancePlans?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_MaintenancePlans?$top=10>

