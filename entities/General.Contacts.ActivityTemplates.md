---
uid: General.Contacts.ActivityTemplates
---
# General.Contacts.ActivityTemplates Entity

Templates for automatical generation of activity from any document. Entity: Cm_Activity_Templates

Default Display Text Format:  
_{Id}_  
Default Search Member:  
_Id_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ActivitySubjectMask](General.Contacts.ActivityTemplates.md#activitysubjectmask) | string (nullable) | A mask that uses fields from the header table of the source document in the specified route and is used to fill the Subject of the generated activity. 
| [AdditionalDays](General.Contacts.ActivityTemplates.md#additionaldays) | int32 | The number of days that will be added to the date in the Header_Date_Field. The result value is set to Start_Time of the activity. [Required] [Default(0)] 
| [Id](General.Contacts.ActivityTemplates.md#id) | guid |  
| [ReminderTime](General.Contacts.ActivityTemplates.md#remindertime) | time (nullable) | Time of the day for the reminder. 
| [SourceDateField](General.Contacts.ActivityTemplates.md#sourcedatefield) | string | A name of a field from the header or the document table of the source document in the specified route, that will be used along with Additional_Days to set the Start_Time of the generated activity. [Required] 
| [StartTime](General.Contacts.ActivityTemplates.md#starttime) | time | The time of the day when the activity starts. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ResponsibleParty](General.Contacts.ActivityTemplates.md#responsibleparty) | [Parties](General.Contacts.Parties.md) (nullable) | If Null the user that starts the generation route is responsible party of the activity. [Filter(multi eq)] |
| [Route](General.Contacts.ActivityTemplates.md#route) | [Routes](Systems.Workflow.Routes.md) | Document generation route that uses this template. [Required] [Filter(multi eq)] |


## Attribute Details

### ActivitySubjectMask

A mask that uses fields from the header table of the source document in the specified route and is used to fill the Subject of the generated activity.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### AdditionalDays

The number of days that will be added to the date in the Header_Date_Field. The result value is set to Start_Time of the activity. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ReminderTime

Time of the day for the reminder.

_Type_: **time (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SourceDateField

A name of a field from the header or the document table of the source document in the specified route, that will be used along with Additional_Days to set the Start_Time of the generated activity. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartTime

The time of the day when the activity starts. [Required]

_Type_: **time**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ResponsibleParty

If Null the user that starts the generation route is responsible party of the activity. [Filter(multi eq)]

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Route

Document generation route that uses this template. [Required] [Filter(multi eq)]

_Type_: **[Routes](Systems.Workflow.Routes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.ActivityTemplates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.ActivityTemplates erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_ActivityTemplates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_ActivityTemplates?$top=10>

