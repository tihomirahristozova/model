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
Name Data Member:  
_ApplicationName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.UI.FormLayouts](Systems.UI.FormLayouts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ApplicationName](Systems.UI.FormLayouts.md#applicationname) | string (64) | The application, which consumes the layout. `Required` `Filter(eq)` `ORD` 
| [DisplayText](Systems.UI.FormLayouts.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [FormName](Systems.UI.FormLayouts.md#formname) | string (64) | The form, for which the layout is applied. `Required` `Filter(eq;like)` 
| [Id](Systems.UI.FormLayouts.md#id) | guid |  
| [Layout](Systems.UI.FormLayouts.md#layout) | byte[] __nullable__ | The byte storage of the layout. 
| [LayoutFormat](Systems.UI.FormLayouts.md#layoutformat) | [LayoutFormat](Systems.UI.FormLayouts.md#layoutformat) | The format of the data in the Layout column. Values can be: 'U' - uncompressed; 'L' - LZO compressed; 'D' - Deflate compressed. `Required` `Default("U")` 
| [LayoutName](Systems.UI.FormLayouts.md#layoutname) | string (64) | The name of a named layout. Standard layouts have empty string names. `Required` `Filter(eq;like)` 
| [<s>LayoutXml</s>](Systems.UI.FormLayouts.md#layoutxml) | string (max) __nullable__ | **OBSOLETE! Do not use!**  
| [<s>MachineName</s>](Systems.UI.FormLayouts.md#machinename) | string (128) __nullable__ | **OBSOLETE! Do not use!**  
| [ObjectVersion](Systems.UI.FormLayouts.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
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
_Category_: **System**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Maximum Length_: **64**  

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### FormName

The form, for which the layout is applied. `Required` `Filter(eq;like)`

_Type_: **string (64)**  
_Category_: **System**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Layout

The byte storage of the layout.

_Type_: **byte[] __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LayoutFormat

The format of the data in the Layout column. Values can be: 'U' - uncompressed; 'L' - LZO compressed; 'D' - Deflate compressed. `Required` `Default("U")`

_Type_: **[LayoutFormat](Systems.UI.FormLayouts.md#layoutformat)**  
_Category_: **System**  
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
_Category_: **System**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### LayoutXml

**OBSOLETE! Do not use!**

_Type_: **string (max) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### MachineName

**OBSOLETE! Do not use!**

_Type_: **string (128) __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### PanelName

The visual panel, for which the layout is applied. `Required` `Default("Form")` `Filter(eq)`

_Type_: **string (64)**  
_Category_: **System**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  
_Default Value_: **Form**  

### UserName

The user for which the layout is applied. null means that the layout is applied for all users. `Filter(eq;like)`

_Type_: **string (64) __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  


## Reference Details

### AccessKey

The security access key which controls the access to the layout view. `Filter(multi eq)`

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### Role

The role, for which the layout is applied. `Filter(multi eq)`

_Type_: **[Roles](Systems.Workflow.Roles.md) (nullable)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  


### CreateNotification

Creates a notification a sends a real time event to the user.  
_Return Type_: **void**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  

**Parameters**  
  * **user**  
    The user.  
    _Type_: [Users](Systems.Security.Users.md)  

  * **notificationClass**  
    The notification class.  
    _Type_: string  

  * **subject**  
    The subject.  
    _Type_: string  


### CreateCopy

Duplicates the object and its child objects belonging to the same aggregate.              The duplicated objects are not saved to the data source but remain in the same transaction as the original object.  
_Return Type_: **EntityObject**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  


## Business Rules

[!list limit=1000 erp.entity=Systems.UI.FormLayouts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.UI.FormLayouts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_UI_FormLayouts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_UI_FormLayouts?$top=10>

