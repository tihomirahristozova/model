---
uid: Systems.Core.ExternalApplications
---
# Systems.Core.ExternalApplications Entity

List of external applications. Used to run external applications. Entity: Sys_External_Applications

Default Display Text Format:  
_{EntityName:T}_  
Default Search Member:  
_EntityName_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Address](Systems.Core.ExternalApplications.md#address) | string | The address (path) to the application. The address is platform-dependant. [Required] 
| [AvailableInMode](Systems.Core.ExternalApplications.md#availableinmode) | [AvailableInMode](Systems.Core.ExternalApplications.md#availableinmode) | Whether the application will be displayed to the end users when a single object is opened or when multiple objects are listed. [Required] [Default("SINGLE")] [Filter(eq)] 
| [EntityName](Systems.Core.ExternalApplications.md#entityname) | string | The entity, for which the application is defined. [Required] [Filter(eq)] [ORD] 
| [ExecuteForAllObjects](Systems.Core.ExternalApplications.md#executeforallobjects) | boolean | Whether to execute the application for all selected objects at once or to execute the application for each object, one by one. [Required] [Default(true)] [Filter(eq)] 
| [Id](Systems.Core.ExternalApplications.md#id) | guid |  
| [IsActive](Systems.Core.ExternalApplications.md#isactive) | boolean (nullable) | Specifies whether the external application is currently used. [Default(true)] [Filter(eq)] 
| [Name](Systems.Core.ExternalApplications.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of the external application. [Required] [Filter(eq;like)] 
| [Notes](Systems.Core.ExternalApplications.md#notes) | string (nullable) | Notes for this ExternalApplication. 
| [Platform](Systems.Core.ExternalApplications.md#platform) | [Platform](Systems.Core.ExternalApplications.md#platform) | The execution platform of the application. [Required] [Filter(eq)] 
| [RefreshAfterFinish](Systems.Core.ExternalApplications.md#refreshafterfinish) | boolean | Whether to refresh the data, displayed to the user, after the execution finishes. Not all platforms and/or applications support finish notification. [Required] [Default(true)] [Filter(eq)] 
| [SaveBeforeStart](Systems.Core.ExternalApplications.md#savebeforestart) | boolean | Whether to save the form data to the server before starting the application. [Required] [Default(true)] [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.Core.ExternalApplications.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this ExternalApplication. Null means that all users have unlimited permissions. [Filter(multi eq)] |


## Attribute Details

### Address

The address (path) to the application. The address is platform-dependant. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### AvailableInMode

Whether the application will be displayed to the end users when a single object is opened or when multiple objects are listed. [Required] [Default("SINGLE")] [Filter(eq)]

_Type_: **[AvailableInMode](Systems.Core.ExternalApplications.md#availableinmode)**  
Allowed values for the [AvailableInMode](Systems.Core.ExternalApplications.md#availableinmode) data attribute  
_Allowed Values (Systems.Core.ExternalApplicationsRepository.AvailableInMode Enum Members)_  

| Value | Description |
| ---- | --- |
| SINGLE | SINGLE value. Stored as 'SINGLE'. <br /> _Database Value:_ 'SINGLE' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'SINGLE' |
| LIST | LIST value. Stored as 'LIST'. <br /> _Database Value:_ 'LIST' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'LIST' |
| ALL | ALL value. Stored as 'ALL'. <br /> _Database Value:_ 'ALL' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'ALL' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **SINGLE**  

### EntityName

The entity, for which the application is defined. [Required] [Filter(eq)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### ExecuteForAllObjects

Whether to execute the application for all selected objects at once or to execute the application for each object, one by one. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the external application is currently used. [Default(true)] [Filter(eq)]

_Type_: **boolean (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

The name of the external application. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this ExternalApplication.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Platform

The execution platform of the application. [Required] [Filter(eq)]

_Type_: **[Platform](Systems.Core.ExternalApplications.md#platform)**  
Allowed values for the [Platform](Systems.Core.ExternalApplications.md#platform) data attribute  
_Allowed Values (Systems.Core.ExternalApplicationsRepository.Platform Enum Members)_  

| Value | Description |
| ---- | --- |
| WINDOWS | WINDOWS value. Stored as 'WINDOWS'. <br /> _Database Value:_ 'WINDOWS' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'WINDOWS' |
| WEBPAGE | WEBPAGE value. Stored as 'WEBPAGE'. <br /> _Database Value:_ 'WEBPAGE' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'WEBPAGE' |
| WEBSERVICE | WEBSERVICE value. Stored as 'WEBSERVICE'. <br /> _Database Value:_ 'WEBSERVICE' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'WEBSERVICE' |
| ANDROID | ANDROID value. Stored as 'ANDROID'. <br /> _Database Value:_ 'ANDROID' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'ANDROID' |
| IOS | IOS value. Stored as 'iOS'. <br /> _Database Value:_ 'iOS' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'IOS' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### RefreshAfterFinish

Whether to refresh the data, displayed to the user, after the execution finishes. Not all platforms and/or applications support finish notification. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### SaveBeforeStart

Whether to save the form data to the server before starting the application. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  


## Reference Details

### AccessKey

The access key, containing the user permissions for this ExternalApplication. Null means that all users have unlimited permissions. [Filter(multi eq)]

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Core.ExternalApplications erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.ExternalApplications erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_ExternalApplications?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_ExternalApplications?$top=10>

