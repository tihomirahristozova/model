---
uid: Applications.Service.ServiceObjectTypes
---
# Applications.Service.ServiceObjectTypes Entity

**Namespace:** [Applications.Service](Applications.Service.md)  

Contins the types of serviceable objects. Entity: Srv_Service_Object_Types

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Service.ServiceObjectTypes](Applications.Service.ServiceObjectTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceObjectTypes.md#id) | guid |  
| [Name](Applications.Service.ServiceObjectTypes.md#name) | string (254) | The name of this ServiceObjectType. `Required` `Filter(eq;like)` 


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this ServiceObjectType. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  



## Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceObjectTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Service.ServiceObjectTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceObjectTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceObjectTypes?$top=10>

