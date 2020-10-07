# Systems.Core.ResolvedConflicts

Contains records of conflicts, which were automatically resolved by update procedures. Entity: Sys_Resolved_Conflicts

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.ResolvedConflicts.md#Id) | guid |  
| [ConflictDescription](Systems.Core.ResolvedConflicts.md#ConflictDescription) | [MultilanguageString](../data-types/MultilanguageString.md) | Description of the conflict. [Required] [ReadOnly] 
| [ResolveConfirmedByUser](Systems.Core.ResolvedConflicts.md#ResolveConfirmedByUser) | boolean | True, when the conflict resolution was manually confirmed by user. [Required] [Default(false)] [Filter(eq)] 
| [ResolveConfirmedTime](Systems.Core.ResolvedConflicts.md#ResolveConfirmedTime) | datetime (nullable) | Time when the conflict resolution was confirmed by the user. [ReadOnly] 
| [ResolveDescription](Systems.Core.ResolvedConflicts.md#ResolveDescription) | [MultilanguageString](../data-types/MultilanguageString.md) | Description of the resolution of the conflict. [Required] [ReadOnly] 
| [ResolvedTime](Systems.Core.ResolvedConflicts.md#ResolvedTime) | datetime | Time when the resolution of the conflict was made. [Required] [Default(Now)] [ReadOnly] 
| [RevisedByUser](Systems.Core.ResolvedConflicts.md#RevisedByUser) | boolean | True, when the conflict resolution was revised (reviewed) manually by user. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [TableName](Systems.Core.ResolvedConflicts.md#TableName) | [MultilanguageString](../data-types/MultilanguageString.md) | Name of the table in which the conflict has occurred. [Required] [Filter(like)] [ReadOnly] 
| [URL](Systems.Core.ResolvedConflicts.md#URL) | string | URL of the item (the row) for which the conflict occurred. [Required] [ReadOnly] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ConflictDescription

> Description of the conflict. [Required] [ReadOnly]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ResolveConfirmedByUser

> True, when the conflict resolution was manually confirmed by user. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ResolveConfirmedTime

> Time when the conflict resolution was confirmed by the user. [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ResolveDescription

> Description of the resolution of the conflict. [Required] [ReadOnly]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ResolvedTime

> Time when the resolution of the conflict was made. [Required] [Default(Now)] [ReadOnly]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### RevisedByUser

> True, when the conflict resolution was revised (reviewed) manually by user. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### TableName

> Name of the table in which the conflict has occurred. [Required] [Filter(like)] [ReadOnly]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### URL

> URL of the item (the row) for which the conflict occurred. [Required] [ReadOnly]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Core.ResolvedConflicts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.ResolvedConflicts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Core.ResolvedConflicts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_ResolvedConflicts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_ResolvedConflicts?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Sys_Resolved_Conflicts?$top=10>

