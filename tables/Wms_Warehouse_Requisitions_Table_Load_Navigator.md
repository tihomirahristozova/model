# Query Wms_Warehouse_Requisitions_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company which issued the document|
|[Document_Date](#document_date)|`date` |The date on which the document was issued|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc.|
|[Document_No](#document_no)|`nvarchar` |Document number, unique within Document_Type_Id|
|[To_Party_Id](#to_party_id)|`uniqueidentifier` |The party which should receive the document|
|[From_Party_Id](#from_party_id)|`uniqueidentifier` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location which issued the document. NULL means that there is only one location within the enterprise company and locations are not used|
|[Planning_Only](#planning_only)|`bit` Readonly|Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned)|
|[Prime_Cause_Document_Id](#prime_cause_document_id)|`uniqueidentifier` |The document that is the prime cause for creation of the current document|
|[Release_Time](#release_time)|`datetime` Readonly|Date and time when the document was released (State set to Released).|
|[Complete_Time](#complete_time)|`datetime` Readonly|Date and time when the document was completed (State set to Completed).|
|[Parent_Document_Relationship_Type](#parent_document_relationship_type)|`nvarchar` Allowed: `S`, `N`, Readonly|Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.|
|[Reference_Document_No](#reference_document_no)|`nvarchar` |The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents|
|[To_Company_Division_Id](#to_company_division_id)|`uniqueidentifier` |The division of the company, receiving the document. NULL when the document is not received by any specific division|
|[From_Company_Division_Id](#from_company_division_id)|`uniqueidentifier` |The division of the company, issuing the document. NULL when the document is not issued by any specific division|
|[Reverse_Of_Document_Id](#reverse_of_document_id)|`uniqueidentifier` Readonly|The document which the current document is reverse of|
|[Entity_Name](#entity_name)|`nvarchar` |The entity name of the document header.|
|[Warehouse_Requisition_Id](#warehouse_requisition_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Warehouse_Id](#warehouse_id)|`uniqueidentifier` |The warehouse, for which the operation is requested.|
|[Requisition_Type](#requisition_type)|`nvarchar` Allowed: `I`, `O`|The type of the requistion. I=Inbound; O=Outbound.|
|[User_Status_Id](#user_status_id)|`uniqueidentifier` Readonly|The user status of this document if applicable for this document type. NULL means unknown or not yet set|
|[Void_Reason](#void_reason)|`nvarchar` Readonly|Reason for voiding the document, entered by the user|
|[Document_Notes](#document_notes)|`nvarchar` ||
|[Document_Version](#document_version)|`int` Readonly|Consecutive version number, starting with 1. Each update produces a new version of the document.|
|[Reference_Date](#reference_date)|`datetime` |The date to which this document refers, i.e. when the action really occurred. If NULL, Document_Date is taken|
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly|The current system state of the document. Allowed values: 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed.|
|[Void](#void)|`bit` Readonly|1 if the document is null and void|
|[Currency_Directory_Id](#currency_directory_id)|`uniqueidentifier` |The currency directory, containing all the convertion rates, used by the document. NULL means that the document does not need currency convertions|
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` |In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |In a multi-document tree, this is the direct parent document. If this is the root it is NULL|
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` Readonly|The primary document, which the current document adjusts. NULL when this is not an adjustment document|
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` |The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.|
|[Adjustment_Number](#adjustment_number)|`int` Readonly|Consecutive number of the correction that this document is applying to the adjusted document.|
|[Creation_User](#creation_user)|`nvarchar` Readonly|The login name of the user, who created the document|
|[Void_Time](#void_time)|`datetime` Readonly|Date/time when the document has become void|
|[Void_User](#void_user)|`nvarchar` Readonly|The user who voided the document|
|[Adjustment_Time](#adjustment_time)|`datetime` Readonly|Date/time when the document last has been adjusted by corrective document|
|[Adjustment_User](#adjustment_user)|`nvarchar` Readonly|The user who adjusted the document|
|[Read_Only](#read_only)|`bit` Readonly|1 - the document is read only; 0 - the document is not read only|
|[Expected_Date](#expected_date)|`date` |Date, when the requisition is expected to be fulfilled.|
|[Creation_Time](#creation_time)|`datetime` Readonly|Date/Time when the document was created|
|[Expected_Time](#expected_time)|`time` |Time, when the requisition is expected to be executed. NULL when the time is unknown.|

## Columns

### Enterprise_Company_Id

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

### From_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planning_Only

| Property | Value |
| - | - |
|Type|bit|

### Prime_Cause_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Release_Time

| Property | Value |
| - | - |
|Type|datetime|

### Complete_Time

| Property | Value |
| - | - |
|Type|datetime|

### Parent_Document_Relationship_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Reference_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### To_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reverse_Of_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Warehouse_Requisition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Requisition_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Void_Reason

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Version

| Property | Value |
| - | - |
|Type|int|

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

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjustment_Number

| Property | Value |
| - | - |
|Type|int|

### Creation_User

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

### Adjustment_Time

| Property | Value |
| - | - |
|Type|datetime|

### Adjustment_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Read_Only

| Property | Value |
| - | - |
|Type|bit|

### Expected_Date

| Property | Value |
| - | - |
|Type|date|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Expected_Time

| Property | Value |
| - | - |
|Type|time|


