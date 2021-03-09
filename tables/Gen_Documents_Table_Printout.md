# Procedure Gen_Documents_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[From_Party_Id](#from_party_id)|`uniqueidentifier` |The party which issued the document|
|[Document_Date](#document_date)|`date` |The date on which the document was issued|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc.|
|[Document_No](#document_no)|`nvarchar` |Document number, unique within Document_Type_Id|
|[To_Party_Id](#to_party_id)|`uniqueidentifier` |The party which should receive the document|
|[Notes](#notes)|`nvarchar` ||
|[Set_State_20_Time](#set_state_20_time)|`datetime` ||
|[Set_State_10_User](#set_state_10_user)|`nvarchar` ||
|[Set_State_30_Time](#set_state_30_time)|`datetime` ||
|[Set_State_30_User](#set_state_30_user)|`nvarchar` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |In a multi-document tree, this is the direct parent document. If this is the root it is NULL|
|[Set_State_10_Time](#set_state_10_time)|`datetime` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location which issued the document. NULL means that there is only one location within the enterprise company and locations are not used|
|[Reverse_Of_Document_Id](#reverse_of_document_id)|`uniqueidentifier` Readonly|The document which the current document is reverse of|
|[Master_Document_Type_Name](#master_document_type_name)|`nvarchar` ||
|[Master_Document_No](#master_document_no)|`nvarchar` ||
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` |In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id|
|[Parent_Document_Type_Name](#parent_document_type_name)|`nvarchar` ||
|[Parent_Document_No](#parent_document_no)|`nvarchar` ||
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` ||
|[Set_State_20_User](#set_state_20_user)|`nvarchar` ||
|[Id](#id)|`uniqueidentifier` `PK`||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly|The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed.|
|[Void](#void)|`bit` Readonly|1 if the document is null and void|
|[From_Party_Id_Text](#from_party_id_text)|`nvarchar` `ML`|The name of the party|
|[Document_Type_Id_Text](#document_type_id_text)|`nvarchar` `ML`|Description of the document type|
|[Entity_Name](#entity_name)|`nvarchar` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id_Text](#enterprise_company_id_text)|`nvarchar` `ML`|The name of the party|
|[To_Party_Id_Text](#to_party_id_text)|`nvarchar` `ML`|The name of the party|
|[Read_Only](#read_only)|`bit` Readonly|1 - the document is read only; 0 - the document is not read only|
|[Creation_Time](#creation_time)|`datetime` Readonly|Date/Time when the document was created|
|[Creation_User_Name](#creation_user_name)|`nvarchar` ||
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` |The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.|
|[Responsible_Person_Id_Text](#responsible_person_id_text)|`nvarchar` `ML`|The name of the party|
|[Void_Time](#void_time)|`datetime` Readonly|Date/time when the document has become void|
|[Void_User](#void_user)|`nvarchar` Readonly|The user who voided the document|
|[Set_State_40_Time](#set_state_40_time)|`datetime` ||
|[Creation_User](#creation_user)|`nvarchar` Readonly|The login name of the user, who created the document|
|[Set_State_40_User](#set_state_40_user)|`nvarchar` ||

## Columns

### From_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Set_State_20_Time

| Property | Value |
| - | - |
|Type|datetime|

### Set_State_10_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Set_State_30_Time

| Property | Value |
| - | - |
|Type|datetime|

### Set_State_30_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Set_State_10_Time

| Property | Value |
| - | - |
|Type|datetime|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reverse_Of_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Master_Document_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Master_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Master_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Document_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Adjusted_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Set_State_20_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### State

| Property | Value |
| - | - |
|Type|smallint|

### Void

| Property | Value |
| - | - |
|Type|bit|

### From_Party_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Type_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### To_Party_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Read_Only

| Property | Value |
| - | - |
|Type|bit|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Responsible_Person_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Void_Time

| Property | Value |
| - | - |
|Type|datetime|

### Void_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Set_State_40_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Set_State_40_User

| Property | Value |
| - | - |
|Type|nvarchar|


