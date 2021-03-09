# Query Pdm_Data_Subject_Right_Requests_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Data_Subject_Right_Request_Id](#data_subject_right_request_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company, to which the request was made.|
|[Person_Id](#person_id)|`uniqueidentifier` |The person, whose data will be corrected with the request. |
|[Created_By_User_Id](#created_by_user_id)|`uniqueidentifier` Readonly|The user account, which was used to create the request. Null when the request was created internally, on behalf of the external person.|
|[Created_On_Utc](#created_on_utc)|`datetime` |The date and time (in UTC), when the request was created.|
|[Requested_Right](#requested_right)|`nvarchar` Allowed: `REC`, `ERA`, `RES`, `POR`, `OBJ`, `OTH`|The requested right, according to GDPR and other personal data regulations.  REC=Rectify; ERA=Erasure; RES=Restrict; POR=Portability; OBJ=Object; OTH=Other.|
|[Completed_By_User_Id](#completed_by_user_id)|`uniqueidentifier` Readonly|The internal user account, which marked the request as implemented. Null when the request is still not implemented, or when the user is unknown.|
|[Completed_On_Utc](#completed_on_utc)|`datetime` |Date and time (in UTC), when the requested right was implemented by the responsible entity. Null if the request is still not implemented.|
|[Notes](#notes)|`nvarchar` |This should usually contain detailed implementation notes.|
|[Status](#status)|`nvarchar` Allowed: `1`, `2`, `3`, `4`, `5`|The status of the request. 1=Requested; 2=Reviewing; 3=Executing; 4=Implemented; 5=Denied.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Data_Subject_Right_Request_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Created_By_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Created_On_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Requested_Right

| Property | Value |
| - | - |
|Type|nvarchar|

### Completed_By_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Completed_On_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Status

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


