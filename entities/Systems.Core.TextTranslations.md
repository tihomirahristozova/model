---
uid: Systems.Core.TextTranslations
---
# Systems.Core.TextTranslations Entity

**Namespace:** [Systems.Core](Systems.Core.md)  

Obsolete. Not used. Entity: Gen_Text_Translations

## Default Visualization
Default Display Text Format:  
_{ColumnName:T}_  
Default Search Member:  
_ColumnName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Core.TextTranslations](Systems.Core.TextTranslations.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ColumnName](Systems.Core.TextTranslations.md#columnname) | string (128) | Obsolete. Not used. `Required` `Filter(eq)` 
| [Id](Systems.Core.TextTranslations.md#id) | guid |  
| [Language](Systems.Core.TextTranslations.md#language) | string (50) | Obsolete. Not used. `Required` `Filter(eq)` 
| [RowId](Systems.Core.TextTranslations.md#rowid) | guid | Obsolete. Not used. `Required` `Filter(multi eq)` 
| [TableName](Systems.Core.TextTranslations.md#tablename) | string (128) | Obsolete. Not used. `Required` `Filter(eq)` `ORD` `ReadOnly` 
| [TranslatedText](Systems.Core.TextTranslations.md#translatedtext) | string (254) __nullable__ | Obsolete. Not used. `Filter(eq)` 


## Attribute Details

### ColumnName

Obsolete. Not used. `Required` `Filter(eq)`

_Type_: **string (128)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Language

Obsolete. Not used. `Required` `Filter(eq)`

_Type_: **string (50)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **50**  

### RowId

Obsolete. Not used. `Required` `Filter(multi eq)`

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  

### TableName

Obsolete. Not used. `Required` `Filter(eq)` `ORD` `ReadOnly`

_Type_: **string (128)**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Maximum Length_: **128**  

### TranslatedText

Obsolete. Not used. `Filter(eq)`

_Type_: **string (254) __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  



## Business Rules

[!list erp.entity=Systems.Core.TextTranslations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.TextTranslations erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_TextTranslations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_TextTranslations?$top=10>

