# Systems.UI.FormLayouts

Contains user layouts of the screen forms. Entity: Sys_Form_Layouts

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.UI.FormLayouts.md#Id) | guid |  
| [ApplicationName](Systems.UI.FormLayouts.md#ApplicationName) | string | The application, which consumes the layout. [Required] [Filter(eq)] [ORD] 
| [FormName](Systems.UI.FormLayouts.md#FormName) | string | The form, for which the layout is applied. [Required] [Filter(eq;like)] 
| [Layout](Systems.UI.FormLayouts.md#Layout) | byte[] (nullable) | The byte storage of the layout. 
| [LayoutFormat](Systems.UI.FormLayouts.md#LayoutFormat) | [Systems.UI.FormLayoutsRepository.LayoutFormat](Systems.UI.FormLayouts.md#LayoutFormat) | The format of the data in the Layout column. Values can be: 'U' - uncompressed; 'L' - LZO compressed; 'D' - Deflate compressed. [Required] [Default("U")] 
| [LayoutName](Systems.UI.FormLayouts.md#LayoutName) | string | The name of a named layout. Standard layouts have empty string names. [Required] [Filter(eq;like)] 
| [PanelName](Systems.UI.FormLayouts.md#PanelName) | string | The visual panel, for which the layout is applied. [Required] [Default("Form")] [Filter(eq)] 
| [UserName](Systems.UI.FormLayouts.md#UserName) | string (nullable) | The user for which the layout is applied. null means that the layout is applied for all users. [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.UI.FormLayouts.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The security access key which controls the access to the layout view. [Filter(multi eq)] |
| [Role](Systems.UI.FormLayouts.md#Role) | [Systems.Workflow.Roles](Systems.Workflow.Roles.md) (nullable) | The role, for which the layout is applied. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ApplicationName

> The application, which consumes the layout. [Required] [Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### FormName

> The form, for which the layout is applied. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Layout

> The byte storage of the layout.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LayoutFormat

> The format of the data in the Layout column. Values can be: 'U' - uncompressed; 'L' - LZO compressed; 'D' - Deflate compressed. [Required] [Default("U")]

_Type_: **[Systems.UI.FormLayoutsRepository.LayoutFormat](Systems.UI.FormLayouts.md#LayoutFormat)**  
Allowed values for the [LayoutFormat](Systems.UI.FormLayouts.md#LayoutFormat) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| CompressedDeflate | CompressedDeflate value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'CompressedDeflate' |
| CompressedLZO | CompressedLZO value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'CompressedLZO' |
| Uncompressed | Uncompressed value. Stored as 'U'. <br /> _Database Value:_ 'U' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Uncompressed' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Uncompressed**  

### LayoutName

> The name of a named layout. Standard layouts have empty string names. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### PanelName

> The visual panel, for which the layout is applied. [Required] [Default("Form")] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Form**  

### UserName

> The user for which the layout is applied. null means that the layout is applied for all users. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

> The security access key which controls the access to the layout view. [Filter(multi eq)]

_Type_: **[Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Role

> The role, for which the layout is applied. [Filter(multi eq)]

_Type_: **[Systems.Workflow.Roles](Systems.Workflow.Roles.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.UI.FormLayouts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.UI.FormLayouts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.UI.FormLayouts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_UI_FormLayouts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_UI_FormLayouts?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Sys_Form_Layouts?$top=10>

