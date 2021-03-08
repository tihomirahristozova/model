# Table Pdm_Data_Subject_Right_Requests

Contains user requests for application of user rights. Entity: Pdm_Data_Subject_Right_Requests (Introduced in version 18.2)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Data_Subject_Right_Request_Id|`Guid`|`PK`, Readonly||
|Completed_On_Utc|`DateTime?`||Date and time (in UTC), when the requested right was implemented by the responsible entity. Null if the request is still not implemented. |
|Created_On_Utc|`DateTime`||The date and time (in UTC), when the request was created. `Required` `Default(Now)` |
|Notes|`String`||This should usually contain detailed implementation notes. |
|Requested_Right|`RequestedRight`|Allowed: `REC`, `ERA`, `RES`, `POR`, `OBJ`, `OTH`|The requested right, according to GDPR and other personal data regulations.  REC=Rectify; ERA=Erasure; RES=Restrict; POR=Portability; OBJ=Object; OTH=Other. `Required` `Filter(eq)` |
|Status|`Status`|Allowed: `1`, `2`, `3`, `4`, `5`|The status of the request. 1=Requested; 2=Reviewing; 3=Executing; 4=Implemented; 5=Denied. `Required` |
