---
uid: Systems.Core.WebHooks
---
# Systems.Core.WebHooks Entity

**Namespace:** [Systems.Core](Systems.Core.md)  

Webhook templates. Activated by business rules or other means. Entity: Sys_Web_Hooks (Introduced in version 22.1.5.8)

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Code; Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Core.WebHooks](Systems.Core.WebHooks.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Body](Systems.Core.WebHooks.md#body) | string (max) __nullable__ | The body of the POST request (interpolated string). 
| [Code](Systems.Core.WebHooks.md#code) | string (32) | The unique code of the WebHook. `Required` `Filter(eq;like)` `ORD` 
| [EntityType](Systems.Core.WebHooks.md#entitytype) | string (128) | The entity type for which the webhook is setup. All interpolated strings will be evaluated in the context of entities of the specified type. `Required` `Filter(eq;like)` 
| [Headers](Systems.Core.WebHooks.md#headers) | string (max) __nullable__ | Optional headers for the request (interpolated string). Each header is specified on a separate line. 
| [Id](Systems.Core.WebHooks.md#id) | guid |  
| [Name](Systems.Core.WebHooks.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Webhook template name (multi-language). `Required` `Filter(like)` 
| [Notes](Systems.Core.WebHooks.md#notes) | string (max) __nullable__ | Notes for this WebHook. 
| [ObjectVersion](Systems.Core.WebHooks.md#objectversion) | int32 |  
| [RetryLogic](Systems.Core.WebHooks.md#retrylogic) | [RetryLogic](Systems.Core.WebHooks.md#retrylogic) | 0=Don't retry (default); 3=Retry up to 3 times. `Required` `Default("0")` 
| [URL](Systems.Core.WebHooks.md#url) | string (2000) | The destination URL, which should be called by the webhook (interpolated string). `Required` 


## Attribute Details

### Body

The body of the POST request (interpolated string).

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Code

The unique code of the WebHook. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (32)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **32**  

### EntityType

The entity type for which the webhook is setup. All interpolated strings will be evaluated in the context of entities of the specified type. `Required` `Filter(eq;like)`

_Type_: **string (128)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### Headers

Optional headers for the request (interpolated string). Each header is specified on a separate line.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Webhook template name (multi-language). `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

Notes for this WebHook.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### RetryLogic

0=Don't retry (default); 3=Retry up to 3 times. `Required` `Default("0")`

_Type_: **[RetryLogic](Systems.Core.WebHooks.md#retrylogic)**  
Allowed values for the `RetryLogic`(Systems.Core.WebHooks.md#retrylogic) data attribute  
_Allowed Values (Systems.Core.WebHooksRepository.RetryLogic Enum Members)_  

| Value | Description |
| ---- | --- |
| NoRetry | NoRetry value. Stored as '0'. <br /> _Database Value:_ '0' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NoRetry' |
| Retry | Retry value. Stored as '3'. <br /> _Database Value:_ '3' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Retry' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **NoRetry**  

### URL

The destination URL, which should be called by the webhook (interpolated string). `Required`

_Type_: **string (2000)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2000**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Core.WebHooks erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Core.WebHooks erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_WebHooks?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_WebHooks?$top=10>

