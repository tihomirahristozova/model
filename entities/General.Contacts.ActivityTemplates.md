---
uid: General.Contacts.ActivityTemplates
---
# General.Contacts.ActivityTemplates Entity

**Namespace:** [General.Contacts](General.Contacts.md)  

Templates for automatical generation of activity from any document. Entity: Cm_Activity_Templates

## Default Visualization
Default Display Text Format:  
_{Id}: {RouteId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Contacts.ActivityTemplates](General.Contacts.ActivityTemplates.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ActivitySubjectMask](General.Contacts.ActivityTemplates.md#activitysubjectmask) | string (max) __nullable__ | A mask that uses fields from the header table of the source document in the specified route and is used to fill the Subject of the generated activity. 
| [AdditionalDays](General.Contacts.ActivityTemplates.md#additionaldays) | int32 | The number of days that will be added to the date in the Header_Date_Field. The result value is set to Start_Time of the activity. `Required` `Default(0)` 
| [DisplayText](General.Contacts.ActivityTemplates.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [Id](General.Contacts.ActivityTemplates.md#id) | guid |  
| [ObjectVersion](General.Contacts.ActivityTemplates.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [ReminderTime](General.Contacts.ActivityTemplates.md#remindertime) | time __nullable__ | Time of the day for the reminder. 
| [SourceDateField](General.Contacts.ActivityTemplates.md#sourcedatefield) | string (64) | A name of a field from the header or the document table of the source document in the specified route, that will be used along with Additional_Days to set the Start_Time of the generated activity. `Required` 
| [StartTime](General.Contacts.ActivityTemplates.md#starttime) | time | The time of the day when the activity starts. `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ResponsibleParty](General.Contacts.ActivityTemplates.md#responsibleparty) | [Parties](General.Contacts.Parties.md) (nullable) | If Null the user that starts the generation route is responsible party of the activity. `Filter(multi eq)` |
| [Route](General.Contacts.ActivityTemplates.md#route) | [Routes](Systems.Workflow.Routes.md) | Document generation route that uses this template. `Required` `Filter(multi eq)` |


## Attribute Details

### ActivitySubjectMask

A mask that uses fields from the header table of the source document in the specified route and is used to fill the Subject of the generated activity.

_Type_: **string (max) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### AdditionalDays

The number of days that will be added to the date in the Header_Date_Field. The result value is set to Start_Time of the activity. `Required` `Default(0)`

_Type_: **int32**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ReminderTime

Time of the day for the reminder.

_Type_: **time __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.StartTime > FromMinutes( 30)), ( obj.StartTime - FromMinutes( 30)), obj.StartTime)`
### SourceDateField

A name of a field from the header or the document table of the source document in the specified route, that will be used along with Additional_Days to set the Start_Time of the generated activity. `Required`

_Type_: **string (64)**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### StartTime

The time of the day when the activity starts. `Required`

_Type_: **time**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ResponsibleParty

If Null the user that starts the generation route is responsible party of the activity. `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### Route

Document generation route that uses this template. `Required` `Filter(multi eq)`

_Type_: **[Routes](Systems.Workflow.Routes.md)**  
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

[!list limit=1000 erp.entity=General.Contacts.ActivityTemplates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Contacts.ActivityTemplates erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_ActivityTemplates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_ActivityTemplates?$top=10>

