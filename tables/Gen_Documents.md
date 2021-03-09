# Table Gen_Documents

Contains all documents issued by and to the enterprise. Entity: Gen_Documents

## Summary

| Name | Type | Description |
| - | - | --- |
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company which issued the document|
|[From_Party_Id](#from_party_id)|`uniqueidentifier` |The party which issued the document|
|[Document_Date](#document_date)|`date` |The date on which the document was issued|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc.|
|[Document_No](#document_no)|`nvarchar(20)` |Document number, unique within Document_Type_Id|
|[To_Party_Id](#to_party_id)|`uniqueidentifier` |The party which should receive the document|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[To_Company_Division_Id](#to_company_division_id)|`uniqueidentifier` |The division of the company, receiving the document. NULL when the document is not received by any specific division|
|[Assigned_To_User_Id](#assigned_to_user_id)|`uniqueidentifier` |The user to which this document is assigned for handling. NULL means that the document is not assigned to specific user|
|[User_Status_Id](#user_status_id)|`uniqueidentifier` Readonly|The user status of this document if applicable for this document type. NULL means unknown or not yet set|
|[Reference_Document_No](#reference_document_no)|`nvarchar(20)` |The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents|
|[Document_Version](#document_version)|`int` Readonly|Consecutive version number, starting with 1. Each update produces a new version of the document.|
|[Parent_Document_Relationship_Type](#parent_document_relationship_type)|`nvarchar(1)` Allowed: `S`, `N`, Readonly|Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.|
|[Complete_Time](#complete_time)|`datetime` Readonly|Date and time when the document was completed (State set to Completed).|
|[Release_Time](#release_time)|`datetime` Readonly|Date and time when the document was released (State set to Released).|
|[Prime_Cause_Document_Id](#prime_cause_document_id)|`uniqueidentifier` |The document that is the prime cause for creation of the current document|
|[Planning_Only](#planning_only)|`bit` Readonly|Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned)|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location which issued the document. NULL means that there is only one location within the enterprise company and locations are not used|
|[Reverse_Of_Document_Id](#reverse_of_document_id)|`uniqueidentifier` Readonly|The document which the current document is reverse of|
|[Void_Reason](#void_reason)|`nvarchar(254)` Readonly|Reason for voiding the document, entered by the user|
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` |The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.|
|[From_Company_Division_Id](#from_company_division_id)|`uniqueidentifier` |The division of the company, issuing the document. NULL when the document is not issued by any specific division|
|[Id](#id)|`uniqueidentifier` `PK`||
|[Void_User](#void_user)|`nvarchar(64)` Readonly|The user who voided the document|
|[Adjustment_User](#adjustment_user)|`nvarchar(64)` Readonly|The user who adjusted the document|
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` |The access key, containing the user permissions for this document. NULL means that all users have unlimited permissions|
|[Sequence_Id](#sequence_id)|`uniqueidentifier` Readonly|The sequence that will be used to give new numbers to the documents of this type|
|[Reference_Date](#reference_date)|`datetime` |The date to which this document refers, i.e. when the action really occurred. If NULL, Document_Date is taken|
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly|The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed.|
|[Void](#void)|`bit` Readonly|1 if the document is null and void|
|[Currency_Directory_Id](#currency_directory_id)|`uniqueidentifier` |The currency directory, containing all the convertion rates, used by the document. NULL means that the document does not need currency convertions|
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` |In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |In a multi-document tree, this is the direct parent document. If this is the root it is NULL|
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` Readonly|The primary document, which the current document adjusts. NULL when this is not an adjustment document|
|[Adjustment_Number](#adjustment_number)|`int` Readonly|Consecutive number of the correction that this document is applying to the adjusted document.|
|[Creation_Time](#creation_time)|`datetime` Readonly|Date/Time when the document was created|
|[Creation_User](#creation_user)|`nvarchar(64)` Readonly|The login name of the user, who created the document|
|[Void_Time](#void_time)|`datetime` Readonly|Date/time when the document has become void|
|[Entity_Name](#entity_name)|`nvarchar(64)` |The entity name of the document header.|
|[Adjustment_Time](#adjustment_time)|`datetime` Readonly|Date/time when the document last has been adjusted by corrective document|
|[Read_Only](#read_only)|`bit` Readonly|1 - the document is read only; 0 - the document is not read only|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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
|Type|nvarchar(20)|

### To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### To_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Assigned_To_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reference_Document_No

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Document_Version

| Property | Value |
| - | - |
|Type|int|

### Parent_Document_Relationship_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Complete_Time

| Property | Value |
| - | - |
|Type|datetime|

### Release_Time

| Property | Value |
| - | - |
|Type|datetime|

### Prime_Cause_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planning_Only

| Property | Value |
| - | - |
|Type|bit|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reverse_Of_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Void_Reason

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Void_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Adjustment_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sequence_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reference_Date

| Property | Value |
| - | - |
|Type|datetime|

### State

| Property | Value |
| - | - |
|Type|smallint|

### Void

| Property | Value |
| - | - |
|Type|bit|

### Currency_Directory_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Master_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjusted_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjustment_Number

| Property | Value |
| - | - |
|Type|int|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Void_Time

| Property | Value |
| - | - |
|Type|datetime|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Adjustment_Time

| Property | Value |
| - | - |
|Type|datetime|

### Read_Only

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


