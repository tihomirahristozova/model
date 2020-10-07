# Systems.Core.TextTranslations

Obsolete. Not used. Entity: Gen_Text_Translations

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.TextTranslations.md#Id) | guid |  
| [ColumnName](Systems.Core.TextTranslations.md#ColumnName) | string | Obsolete. Not used. [Required] [Filter(eq)] 
| [Language](Systems.Core.TextTranslations.md#Language) | string | Obsolete. Not used. [Required] [Filter(eq)] 
| [RowId](Systems.Core.TextTranslations.md#RowId) | guid | Obsolete. Not used. [Required] [Filter(multi eq)] 
| [TableName](Systems.Core.TextTranslations.md#TableName) | string | Obsolete. Not used. [Required] [Filter(eq)] [ORD] [ReadOnly] 
| [TranslatedText](Systems.Core.TextTranslations.md#TranslatedText) | string (nullable) | Obsolete. Not used. [Filter(eq)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ColumnName

> Obsolete. Not used. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Language

> Obsolete. Not used. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### RowId

> Obsolete. Not used. [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TableName

> Obsolete. Not used. [Required] [Filter(eq)] [ORD] [ReadOnly]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### TranslatedText

> Obsolete. Not used. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Core.TextTranslations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.TextTranslations erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Core.TextTranslations erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_TextTranslations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_TextTranslations?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Text_Translations?$top=10>

