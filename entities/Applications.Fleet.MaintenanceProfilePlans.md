---
uid: Applications.Fleet.MaintenanceProfilePlans
---
# Applications.Fleet.MaintenanceProfilePlans Entity

**Namespace:** [Applications.Fleet](Applications.Fleet.md)  

Contains the plans, included in the maintenance profile. Entity: Fleet_Maintenance_Profile_Plans

## Default Visualization
Default Display Text Format:  
_{MaintenanceProfile.Name}_  
Default Search Members:  
_MaintenanceProfile.Name_  
Name Data Member:  
_MaintenanceProfile.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Fleet.MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md)  
Aggregate Root:  
[Applications.Fleet.MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](Applications.Fleet.MaintenanceProfilePlans.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [Id](Applications.Fleet.MaintenanceProfilePlans.md#id) | guid |  
| [IsActive](Applications.Fleet.MaintenanceProfilePlans.md#isactive) | boolean | True if the maintenance plan is active for this profile. When a plan is not active, maintenance for it will not occur for the current profile. `Required` `Default(true)` `Introduced in version 18.2` 
| [Notes](Applications.Fleet.MaintenanceProfilePlans.md#notes) | string (max) __nullable__ | Notes for this MaintenanceProfilePlan. 
| [ObjectVersion](Applications.Fleet.MaintenanceProfilePlans.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenancePlan](Applications.Fleet.MaintenanceProfilePlans.md#maintenanceplan) | [MaintenancePlans](Applications.Fleet.MaintenancePlans.md) | The maintenance plan, which is included in the profile. `Required` `Filter(multi eq)` |
| [MaintenanceProfile](Applications.Fleet.MaintenanceProfilePlans.md#maintenanceprofile) | [MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md) | The maintenance profile, which includes the plan. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

True if the maintenance plan is active for this profile. When a plan is not active, maintenance for it will not occur for the current profile. `Required` `Default(true)` `Introduced in version 18.2`

_Type_: **boolean**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

Notes for this MaintenanceProfilePlan.

_Type_: **string (max) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### MaintenancePlan

The maintenance plan, which is included in the profile. `Required` `Filter(multi eq)`

_Type_: **[MaintenancePlans](Applications.Fleet.MaintenancePlans.md)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### MaintenanceProfile

The maintenance profile, which includes the plan. `Required` `Filter(multi eq)` `Owner`

_Type_: **[MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  


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


### CreateNotification

Creates a notification a sends a real time event to the user.  
_Return Type_: **void**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  

**Parameters**  
  * **user**  
    The user.  
    _Type_: [Users](Systems.Security.Users.md)  

  * **notificationClass**  
    The notification class.  
    _Type_: string  

  * **subject**  
    The subject.  
    _Type_: string  


### CreateCopy

Duplicates the object and its child objects belonging to the same aggregate.              The duplicated objects are not saved to the data source but remain in the same transaction as the original object.  
_Return Type_: **EntityObject**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  


## Business Rules

[!list limit=1000 erp.entity=Applications.Fleet.MaintenanceProfilePlans erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Fleet.MaintenanceProfilePlans erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_MaintenanceProfilePlans?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_MaintenanceProfilePlans?$top=10>

