---
uid: Systems.Core.AttributeChanges
---
# Systems.Core.AttributeChanges

Attribute values of an object change. Entity: Sys_Attribute_Changes_View

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AttributeName](Systems.Core.AttributeChanges.md#attributename) | string | The attribute name. [Required] [Filter(eq)] 
| [NewValue](Systems.Core.AttributeChanges.md#newvalue) | string (nullable) | The new value. [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ObjectChange](Systems.Core.AttributeChanges.md#objectchange) | [Systems.Core.ObjectChanges](Systems.Core.ObjectChanges.md) | The object change. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### AttributeName

> The attribute name. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### NewValue

> The new value. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### ObjectChange

> The object change. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Core.ObjectChanges](Systems.Core.ObjectChanges.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Core.AttributeChanges erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.AttributeChanges erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Core.AttributeChanges erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_AttributeChanges?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_AttributeChanges?$top=10>

