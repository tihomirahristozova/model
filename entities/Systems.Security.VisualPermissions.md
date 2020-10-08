---
uid: Systems.Security.VisualPermissions
---
# Systems.Security.VisualPermissions

Contains permissions, which are honored only by client applications and are used to provide access to (primarily show/hide) different elements of the user interface. Entity: Sec_Visual_Permissions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.VisualPermissions.md#Id) | guid |  
| [ApplicationName](Systems.Security.VisualPermissions.md#ApplicationName) | string | The application for which the permission is specified. [Required] [Filter(eq)] 
| [ElementName](Systems.Security.VisualPermissions.md#ElementName) | string (nullable) | Optionally, the element from the panel which will be secured. [Filter(eq)] 
| [FormName](Systems.Security.VisualPermissions.md#FormName) | string (nullable) | Optionally, the form which will be secured. [Filter(eq)] 
| [OperationName](Systems.Security.VisualPermissions.md#OperationName) | string (nullable) | Optionally, the operation on the element which will be secured. [Filter(eq)] 
| [PanelName](Systems.Security.VisualPermissions.md#PanelName) | string (nullable) | Optionally, the panel from the form which will be secured. [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.Security.VisualPermissions.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The security access key which controls the access to the visual permission. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ApplicationName

> The application for which the permission is specified. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ElementName

> Optionally, the element from the panel which will be secured. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### FormName

> Optionally, the form which will be secured. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### OperationName

> Optionally, the operation on the element which will be secured. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### PanelName

> Optionally, the panel from the form which will be secured. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

> The security access key which controls the access to the visual permission. [Filter(multi eq)]

_Type_: **[Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Security.VisualPermissions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.VisualPermissions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Security.VisualPermissions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_VisualPermissions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_VisualPermissions?$top=10>

