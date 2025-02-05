---
uid: General.PrintoutLayouts
---
# General.PrintoutLayouts Entity

**Namespace:** [General](General.md)  

Contains design layouts for document printouts. Entity: Gen_Printout_Layouts

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  
Name Data Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.PrintoutLayouts](General.PrintoutLayouts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BinaryLayout](General.PrintoutLayouts.md#binarylayout) | byte[] __nullable__ | The printout layout, when the format requires binary storage. Alternative to Layout. 
| [DisplayText](General.PrintoutLayouts.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [DocumentEntityName](General.PrintoutLayouts.md#documententityname) | string (64) | The entity name of the document type e.g. Crm_Sales_Orders, Inv_Store_Orders etc. `Required` `Filter(eq)` 
| [Id](General.PrintoutLayouts.md#id) | guid |  
| [Layout](General.PrintoutLayouts.md#layout) | string (max) __nullable__ | The textual representation of the printout layout, when the format requires text representation. Alternative to Binary_Layout. 
| [LayoutFormat](General.PrintoutLayouts.md#layoutformat) | string (32) | Format specifier of the layout. Recognized by the application. `Required` `Filter(multi eq)` 
| [Name](General.PrintoutLayouts.md#name) | string (64) | The name of this PrintoutLayout. `Required` `Filter(eq;like)` `ORD` 
| [Notes](General.PrintoutLayouts.md#notes) | string (254) __nullable__ | Notes for this PrintoutLayout. 
| [ObjectVersion](General.PrintoutLayouts.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataSource](General.PrintoutLayouts.md#datasource) | [DataSources](Systems.Reporting.DataSources.md) (nullable) | The data source for the printout. `Filter(multi eq)` |


## Attribute Details

### BinaryLayout

The printout layout, when the format requires binary storage. Alternative to Layout.

_Type_: **byte[] __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### DocumentEntityName

The entity name of the document type e.g. Crm_Sales_Orders, Inv_Store_Orders etc. `Required` `Filter(eq)`

_Type_: **string (64)**  
_Category_: **System**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Layout

The textual representation of the printout layout, when the format requires text representation. Alternative to Binary_Layout.

_Type_: **string (max) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### LayoutFormat

Format specifier of the layout. Recognized by the application. `Required` `Filter(multi eq)`

_Type_: **string (32)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### Name

The name of this PrintoutLayout. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (64)**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **64**  

_Front-End Recalc Expressions:_  
`IIF( Not( IsNullOrEmpty( obj.DocumentEntityName)), obj.GetDefaultName( ), null)`
### Notes

Notes for this PrintoutLayout.

_Type_: **string (254) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### DataSource

The data source for the printout. `Filter(multi eq)`

_Type_: **[DataSources](Systems.Reporting.DataSources.md) (nullable)**  
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

[!list limit=1000 erp.entity=General.PrintoutLayouts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.PrintoutLayouts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_PrintoutLayouts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_PrintoutLayouts?$top=10>

