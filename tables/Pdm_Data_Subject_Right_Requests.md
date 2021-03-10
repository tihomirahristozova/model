# Table Pdm_Data_Subject_Right_Requests

Contains user requests for application of user rights. Entity: Pdm_Data_Subject_Right_Requests (Introduced in version 18.2)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Data_Subject_Right_Request_Id](#data_subject_right_request_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company, to which the request was made.|
|[Person_Id](#person_id)|`uniqueidentifier` |The person, whose data will be corrected with the request. |
|[Created_By_User_Id](#created_by_user_id)|`uniqueidentifier` Readonly|The user account, which was used to create the request. Null when the request was created internally, on behalf of the external person.|
|[Created_On_Utc](#created_on_utc)|`datetime` |The date and time (in UTC), when the request was created.|
|[Requested_Right](#requested_right)|`nvarchar(3)` Allowed: `REC`, `ERA`, `RES`, `POR`, `OBJ`, `OTH`|The requested right, according to GDPR and other personal data regulations.  REC=Rectify; ERA=Erasure; RES=Restrict; POR=Portability; OBJ=Object; OTH=Other.|
|[Completed_By_User_Id](#completed_by_user_id)|`uniqueidentifier` Readonly|The internal user account, which marked the request as implemented. Null when the request is still not implemented, or when the user is unknown.|
|[Completed_On_Utc](#completed_on_utc)|`datetime` |Date and time (in UTC), when the requested right was implemented by the responsible entity. Null if the request is still not implemented.|
|[Notes](#notes)|`nvarchar(2147483647)` |This should usually contain detailed implementation notes.|
|[Status](#status)|`nvarchar(1)` Allowed: `1`, `2`, `3`, `4`, `5`|The status of the request. 1=Requested; 2=Reviewing; 3=Executing; 4=Implemented; 5=Denied.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Data_Subject_Right_Request_Id


Data_Subject_Right_Request_Id

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
|Derived From|[Pdm_Data_Subject_Right_Requests](Pdm_Data_Subject_Right_Requests.md).[Data_Subject_Right_Request_Id](Pdm_Data_Subject_Right_Requests.md#data_subject_right_request_id)|
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

### Enterprise_Company_Id


Enterprise_Company_Id


The enterprise company, to which the request was made.


The enterprise company, to which the request was made.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Data_Subject_Right_Requests](Pdm_Data_Subject_Right_Requests.md).[Enterprise_Company_Id](Pdm_Data_Subject_Right_Requests.md#enterprise_company_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Person_Id


Person_Id


The person, whose data will be corrected with the request. 


The person, whose data will be corrected with the request. 

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Persons](Cm_Persons.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Data_Subject_Right_Requests](Pdm_Data_Subject_Right_Requests.md).[Person_Id](Pdm_Data_Subject_Right_Requests.md#person_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Created_By_User_Id


Created_By_User_Id


The user account, which was used to create the request. Null when the request was created internally, on behalf of the external person.


The user account, which was used to create the request. Null when the request was created internally, on behalf of the external person.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Data_Subject_Right_Requests](Pdm_Data_Subject_Right_Requests.md).[Created_By_User_Id](Pdm_Data_Subject_Right_Requests.md#created_by_user_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Created_On_Utc


Created_On_Utc


The date and time (in UTC), when the request was created.


The date and time (in UTC), when the request was created.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTime|
|Derived From|[Pdm_Data_Subject_Right_Requests](Pdm_Data_Subject_Right_Requests.md).[Created_On_Utc](Pdm_Data_Subject_Right_Requests.md#created_on_utc)|
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

### Requested_Right


Requested_Right


The requested right, according to GDPR and other personal data regulations.  REC=Rectify; ERA=Erasure; RES=Restrict; POR=Portability; OBJ=Object; OTH=Other.


The requested right, according to GDPR and other personal data regulations.  REC=Rectify; ERA=Erasure; RES=Restrict; POR=Portability; OBJ=Object; OTH=Other.

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`REC`, `ERA`, `RES`, `POR`, `OBJ`, `OTH`|
|Default Value|None|
|Derived From|[Pdm_Data_Subject_Right_Requests](Pdm_Data_Subject_Right_Requests.md).[Requested_Right](Pdm_Data_Subject_Right_Requests.md#requested_right)|
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
|Max Length|3|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Completed_By_User_Id


Completed_By_User_Id


The internal user account, which marked the request as implemented. Null when the request is still not implemented, or when the user is unknown.


The internal user account, which marked the request as implemented. Null when the request is still not implemented, or when the user is unknown.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Data_Subject_Right_Requests](Pdm_Data_Subject_Right_Requests.md).[Completed_By_User_Id](Pdm_Data_Subject_Right_Requests.md#completed_by_user_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Completed_On_Utc


Completed_On_Utc


Date and time (in UTC), when the requested right was implemented by the responsible entity. Null if the request is still not implemented.


Date and time (in UTC), when the requested right was implemented by the responsible entity. Null if the request is still not implemented.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Data_Subject_Right_Requests](Pdm_Data_Subject_Right_Requests.md).[Completed_On_Utc](Pdm_Data_Subject_Right_Requests.md#completed_on_utc)|
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

### Notes


Notes


This should usually contain detailed implementation notes.


This should usually contain detailed implementation notes.

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
|Derived From|[Pdm_Data_Subject_Right_Requests](Pdm_Data_Subject_Right_Requests.md).[Notes](Pdm_Data_Subject_Right_Requests.md#notes)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Status


Status


The status of the request. 1=Requested; 2=Reviewing; 3=Executing; 4=Implemented; 5=Denied.


The status of the request. 1=Requested; 2=Reviewing; 3=Executing; 4=Implemented; 5=Denied.

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`1`, `2`, `3`, `4`, `5`|
|Default Value|None|
|Derived From|[Pdm_Data_Subject_Right_Requests](Pdm_Data_Subject_Right_Requests.md).[Status](Pdm_Data_Subject_Right_Requests.md#status)|
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
|Max Length|1|
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
|Derived From|[Pdm_Data_Subject_Right_Requests](Pdm_Data_Subject_Right_Requests.md).[Row_Version](Pdm_Data_Subject_Right_Requests.md#row_version)|
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


