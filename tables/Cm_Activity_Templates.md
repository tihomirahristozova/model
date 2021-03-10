# Table Cm_Activity_Templates

Templates for automatical generation of activity from any document. Entity: Cm_Activity_Templates

## Summary

| Name | Type | Description |
| - | - | --- |
|[Activity_Template_Id](#activity_template_id)|`uniqueidentifier` `PK`||
|[Route_Id](#route_id)|`uniqueidentifier` ||
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` |If Null the user that starts the generation route is responsible party of the activity.|
|[Activity_Subject_Mask](#activity_subject_mask)|`nvarchar(2147483647)` |A mask that uses fields from the header table of the source document in the specified route and is used to fill the Subject of the generated activity.|
|[Source_Date_Field](#source_date_field)|`nvarchar(64)` |A name of a field from the header or the document table of the source document in the specified route, that will be used along with Additional_Days to set the Start_Time of the generated activity.|
|[Additional_Days](#additional_days)|`int` |The number of days that will be added to the date in the Header_Date_Field. The result value is set to Start_Time of the activity.|
|[Start_Time](#start_time)|`time` |The time of the day when the activity starts|
|[Reminder_Time](#reminder_time)|`time` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Activity_Template_Id


Activity_Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Cm_Activity_Templates](Cm_Activity_Templates.md).[Activity_Template_Id](Cm_Activity_Templates.md#activity_template_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Route_Id


Route_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wf_Routes](Wf_Routes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Activity_Templates](Cm_Activity_Templates.md).[Route_Id](Cm_Activity_Templates.md#route_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Responsible_Party_Id


Responsible_Party_Id


If Null the user that starts the generation route is responsible party of the activity.


If Null the user that starts the generation route is responsible party of the activity.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Activity_Templates](Cm_Activity_Templates.md).[Responsible_Party_Id](Cm_Activity_Templates.md#responsible_party_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Activity_Subject_Mask


Activity_Subject_Mask


A mask that uses fields from the header table of the source document in the specified route and is used to fill the Subject of the generated activity.


A mask that uses fields from the header table of the source document in the specified route and is used to fill the Subject of the generated activity.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Activity_Templates](Cm_Activity_Templates.md).[Activity_Subject_Mask](Cm_Activity_Templates.md#activity_subject_mask)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Source_Date_Field


Source_Date_Field


A name of a field from the header or the document table of the source document in the specified route, that will be used along with Additional_Days to set the Start_Time of the generated activity.


A name of a field from the header or the document table of the source document in the specified route, that will be used along with Additional_Days to set the Start_Time of the generated activity.

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Activity_Templates](Cm_Activity_Templates.md).[Source_Date_Field](Cm_Activity_Templates.md#source_date_field)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Additional_Days


Additional_Days


The number of days that will be added to the date in the Header_Date_Field. The result value is set to Start_Time of the activity.


The number of days that will be added to the date in the Header_Date_Field. The result value is set to Start_Time of the activity.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Cm_Activity_Templates](Cm_Activity_Templates.md).[Additional_Days](Cm_Activity_Templates.md#additional_days)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Start_Time


Start_Time


The time of the day when the activity starts


The time of the day when the activity starts

| Property | Value |
| - | - |
|Type|time|
|DateTime Format|Time|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Activity_Templates](Cm_Activity_Templates.md).[Start_Time](Cm_Activity_Templates.md#start_time)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Reminder_Time


Reminder_Time

| Property | Value |
| - | - |
|Type|time|
|DateTime Format|Time|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Activity_Templates](Cm_Activity_Templates.md).[Reminder_Time](Cm_Activity_Templates.md#reminder_time)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Activity_Templates](Cm_Activity_Templates.md).[Row_Version](Cm_Activity_Templates.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


