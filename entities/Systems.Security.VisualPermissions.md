---
uid: Systems.Security.VisualPermissions
---
# Systems.Security.VisualPermissions Entity

**Namespace:** [Systems.Security](Systems.Security.md)  

Contains permissions, which are honored only by client applications and are used to provide access to (primarily show/hide) different elements of the user interface. Entity: Sec_Visual_Permissions

## Default Visualization
Default Display Text Format:  
_{ApplicationName}_  
Default Search Members:  
_ApplicationName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Security.VisualPermissions](Systems.Security.VisualPermissions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ApplicationName](Systems.Security.VisualPermissions.md#applicationname) | string (64) | The application for which the permission is specified. `Required` `Filter(eq)` 
| [ElementName](Systems.Security.VisualPermissions.md#elementname) | string (4000) __nullable__ | Optionally, the element from the panel which will be secured. `Filter(eq)` 
| [FormName](Systems.Security.VisualPermissions.md#formname) | string (128) __nullable__ | Optionally, the form which will be secured. `Filter(eq)` 
| [Id](Systems.Security.VisualPermissions.md#id) | guid |  
| [ObjectVersion](Systems.Security.VisualPermissions.md#objectversion) | int32 |  
| [OperationName](Systems.Security.VisualPermissions.md#operationname) | string (64) __nullable__ | Optionally, the operation on the element which will be secured. `Filter(eq)` 
| [PanelName](Systems.Security.VisualPermissions.md#panelname) | string (128) __nullable__ | Optionally, the panel from the form which will be secured. `Filter(eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.Security.VisualPermissions.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The security access key which controls the access to the visual permission. `Filter(multi eq)` |


## Attribute Details

### ApplicationName

The application for which the permission is specified. `Required` `Filter(eq)`

_Type_: **string (64)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### ElementName

Optionally, the element from the panel which will be secured. `Filter(eq)`

_Type_: **string (4000) __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **4000**  

### FormName

Optionally, the form which will be secured. `Filter(eq)`

_Type_: **string (128) __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### OperationName

Optionally, the operation on the element which will be secured. `Filter(eq)`

_Type_: **string (64) __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### PanelName

Optionally, the panel from the form which will be secured. `Filter(eq)`

_Type_: **string (128) __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  


## Reference Details

### AccessKey

The security access key which controls the access to the visual permission. `Filter(multi eq)`

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Security.VisualPermissions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Security.VisualPermissions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_VisualPermissions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_VisualPermissions?$top=10>

