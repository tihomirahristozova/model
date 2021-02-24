---
uid: Systems.Core.Translations
---
# Systems.Core.Translations Entity

**Namespace:** [Systems.Core](Systems.Core.md)  

Contains user-defined translations for non-english languages of the user interface and program messages. Entity: Sys_Translations

## Default Visualization
Default Display Text Format:  
_{ApplicationName:T}_  
Default Search Member:  
_ApplicationName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Core.Translations](Systems.Core.Translations.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Active](Systems.Core.Translations.md#active) | boolean | True when the translation is verified and activated. [Required] [Default(true)] [Filter(eq)] 
| [ApplicationName](Systems.Core.Translations.md#applicationname) | string (nullable) | The application, containing the resource. For base resource types (T,C,H), this is null. [Filter(eq)] [ORD] 
| [CreationTime](Systems.Core.Translations.md#creationtime) | datetime | Timestamp when the translation was first created. [Required] [Default(Now)] [Filter(ge;le)] [ReadOnly] 
| [Id](Systems.Core.Translations.md#id) | guid |  
| [Language](Systems.Core.Translations.md#language) | string | The code of the language or language-culture pair. Standard Windows codes are used. English="en"; US English = "en-us". [Required] [Default("en")] [Filter(eq)] 
| [ResourceId](Systems.Core.Translations.md#resourceid) | string | The unique identifier of the translated resource. Should use ASCII/English chars only. Shorter strings are suggested. Depending on Text_Type: T:TableName; C:ColumnName; H:TableName.ColumnName; E,M,S: Application specific code. [Required] [Filter(eq;like)] 
| [ResourceType](Systems.Core.Translations.md#resourcetype) | [ResourceType](Systems.Core.Translations.md#resourcetype) | T=Table (entity) Name; C=Column Name; H=Column Hint; R=Meta Resource; E=Error; M=Message; S=Other application specific String. [Required] [Default("S")] [Filter(eq)] 
| [TranslationField](Systems.Core.Translations.md#translationfield) | string | The translated text. [Required] 
| [UpdateTime](Systems.Core.Translations.md#updatetime) | datetime | When the translation was last updated. [Required] [Default(Now)] [ReadOnly] 


## Attribute Details

### Active

True when the translation is verified and activated. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

_Front-End Recalc Expressions:_  
`IIF( Not( IsNullOrEmpty( obj.TranslationField)), True, obj.Active)`
### ApplicationName

The application, containing the resource. For base resource types (T,C,H), this is null. [Filter(eq)] [ORD]

_Type_: **string (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### CreationTime

Timestamp when the translation was first created. [Required] [Default(Now)] [Filter(ge;le)] [ReadOnly]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Language

The code of the language or language-culture pair. Standard Windows codes are used. English="en"; US English = "en-us". [Required] [Default("en")] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **en**  

### ResourceId

The unique identifier of the translated resource. Should use ASCII/English chars only. Shorter strings are suggested. Depending on Text_Type: T:TableName; C:ColumnName; H:TableName.ColumnName; E,M,S: Application specific code. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ResourceType

T=Table (entity) Name; C=Column Name; H=Column Hint; R=Meta Resource; E=Error; M=Message; S=Other application specific String. [Required] [Default("S")] [Filter(eq)]

_Type_: **[ResourceType](Systems.Core.Translations.md#resourcetype)**  
Allowed values for the [ResourceType](Systems.Core.Translations.md#resourcetype) data attribute  
_Allowed Values (Systems.Core.TranslationsRepository.ResourceType Enum Members)_  

| Value | Description |
| ---- | --- |
| TableName | TableName value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'TableName' |
| ColumnName | ColumnName value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'ColumnName' |
| ColumnHint | ColumnHint value. Stored as 'H'. <br /> _Database Value:_ 'H' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'ColumnHint' |
| MetaResource | MetaResource value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'MetaResource' |
| ErrorMessage | ErrorMessage value. Stored as 'E'. <br /> _Database Value:_ 'E' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'ErrorMessage' |
| Message | Message value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Message' |
| OtherApplicationSpecific | OtherApplicationSpecific value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'OtherApplicationSpecific' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **OtherApplicationSpecific**  

### TranslationField

The translated text. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UpdateTime

When the translation was last updated. [Required] [Default(Now)] [ReadOnly]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  



## Business Rules

[!list erp.entity=Systems.Core.Translations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.Translations erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_Translations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_Translations?$top=10>

