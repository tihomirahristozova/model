# General.DocumentManualDistributedAmounts

Obsolete. Not used. Entity: Gen_Document_Manual_Distributed_Amounts

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentManualDistributedAmounts.md#Id) | guid |  
| [DocumentAmountTypeId](General.DocumentManualDistributedAmounts.md#DocumentAmountTypeId) | guid | Obsolete. Not used. [Required] [Filter(multi eq)] 
| [DocumentId](General.DocumentManualDistributedAmounts.md#DocumentId) | guid | Obsolete. Not used. [Required] [Filter(multi eq)] 
| [DocumentLineId](General.DocumentManualDistributedAmounts.md#DocumentLineId) | guid | Obsolete. Not used. [Required] [Filter(multi eq)] 
| [LinePercent](General.DocumentManualDistributedAmounts.md#LinePercent) | decimal | Obsolete. Not used. [Required] 
| [ProductId](General.DocumentManualDistributedAmounts.md#ProductId) | guid | Obsolete. Not used. [Required] [Filter(multi eq)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DocumentAmountTypeId

> Obsolete. Not used. [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DocumentId

> Obsolete. Not used. [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DocumentLineId

> Obsolete. Not used. [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### LinePercent

> Obsolete. Not used. [Required]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProductId

> Obsolete. Not used. [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.DocumentManualDistributedAmounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentManualDistributedAmounts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentManualDistributedAmounts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentManualDistributedAmounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentManualDistributedAmounts?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Document_Manual_Distributed_Amounts?$top=10>

