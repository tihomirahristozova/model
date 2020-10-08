---
uid: Applications.Service.ServiceObjectTypes
---
# Applications.Service.ServiceObjectTypes

Contins the types of serviceable objects. Entity: Srv_Service_Object_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceObjectTypes.md#id) | guid |  
| [Name](Applications.Service.ServiceObjectTypes.md#name) | string | The name of this ServiceObjectType. [Required] [Filter(eq;like)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> The name of this ServiceObjectType. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Service.ServiceObjectTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceObjectTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Service.ServiceObjectTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceObjectTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceObjectTypes?$top=10>

