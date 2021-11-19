---
uid: Systems.UI.FormLayouts
---
# Systems.UI.FormLayouts Entity

**Namespace:** [Systems.UI](Systems.UI.md)  

Contains user layouts of the screen forms. Entity: Sys_Form_Layouts

## Default Visualization
Default Display Text Format:  
_{ApplicationName}_  
Default Search Members:  
_ApplicationName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.UI.FormLayouts](Systems.UI.FormLayouts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ApplicationName](Systems.UI.FormLayouts.md#applicationname) | string (64) | The application, which consumes the layout. `Required` `Filter(eq)` `ORD` 
| [FormName](Systems.UI.FormLayouts.md#formname) | string (64) | The form, for which the layout is applied. `Required` `Filter(eq;like)` 
| [Id](Systems.UI.FormLayouts.md#id) | guid |  
| [Layout](Systems.UI.FormLayouts.md#layout) | byte[] __nullable__ | The byte storage of the layout. 
| [LayoutFormat](Systems.UI.FormLayouts.md#layoutformat) | [LayoutFormat](Systems.UI.FormLayouts.md#layoutformat) | The format of the data in the Layout column. Values can be: 'U' - uncompressed; 'L' - LZO compressed; 'D' - Deflate compressed. `Required` `Default("U")` 
| [LayoutName](Systems.UI.FormLayouts.md#layoutname) | string (64) | The name of a named layout. Standard layouts have empty string names. `Required` `Filter(eq;like)` 
| [PanelName](Systems.UI.FormLayouts.md#panelname) | string (64) | The visual panel, for which the layout is applied. `Required` `Default("Form")` `Filter(eq)` 
| [UserName](Systems.UI.FormLayouts.md#username) | string (64) __nullable__ | The user for which the layout is applied. null means that the layout is applied for all users. `Filter(eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.UI.FormLayouts.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The security access key which controls the access to the layout view. `Filter(multi eq)` |
| [Role](Systems.UI.FormLayouts.md#role) | [Roles](Systems.Workflow.Roles.md) (nullable) | The role, for which the layout is applied. `Filter(multi eq)` |


## Attribute Details

### ApplicationName

The application, which consumes the layout. `Required` `Filter(eq)` `ORD`

_Type_: **string (64)**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Maximum Length_: **64**  

### FormName

The form, for which the layout is applied. `Required` `Filter(eq;like)`

_Type_: **string (64)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Layout

The byte storage of the layout.

_Type_: **byte[] __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LayoutFormat

The format of the data in the Layout column. Values can be: 'U' - uncompressed; 'L' - LZO compressed; 'D' - Deflate compressed. `Required` `Default("U")`

_Type_: **[LayoutFormat](Systems.UI.FormLayouts.md#layoutformat)**  
Allowed values for the `LayoutFormat`(Systems.UI.FormLayouts.md#layoutformat) data attribute  
_Allowed Values (Systems.UI.FormLayoutsRepository.LayoutFormat Enum Members)_  

| Value | Description |
| ---- | --- |
| CompressedDeflate | CompressedDeflate value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'CompressedDeflate' |
| CompressedLZO | CompressedLZO value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'CompressedLZO' |
| Uncompressed | Uncompressed value. Stored as 'U'. <br /> _Database Value:_ 'U' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Uncompressed' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Uncompressed**  

### LayoutName

The name of a named layout. Standard layouts have empty string names. `Required` `Filter(eq;like)`

_Type_: **string (64)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### PanelName

The visual panel, for which the layout is applied. `Required` `Default("Form")` `Filter(eq)`

_Type_: **string (64)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  
_Default Value_: **Form**  

### UserName

The user for which the layout is applied. null means that the layout is applied for all users. `Filter(eq;like)`

_Type_: **string (64) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  


## Reference Details

### AccessKey

The security access key which controls the access to the layout view. `Filter(multi eq)`

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Role

The role, for which the layout is applied. `Filter(multi eq)`

_Type_: **[Roles](Systems.Workflow.Roles.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Systems.UI.FormLayouts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.UI.FormLayouts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_UI_FormLayouts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_UI_FormLayouts?$top=10>

