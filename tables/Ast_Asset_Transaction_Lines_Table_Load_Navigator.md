# Query Ast_Asset_Transaction_Lines_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[From_Party_Id](#from_party_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Document_No](#document_no)|`nvarchar` ||
|[Document_Date](#document_date)|`date` ||
|[Reference_Date](#reference_date)|`datetime` ||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[Void](#void)|`bit` Readonly||
|[To_Party_Id](#to_party_id)|`uniqueidentifier` ||
|[Currency_Directory_Id](#currency_directory_id)|`uniqueidentifier` ||
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` ||
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` ||
|[Adjustment_Number](#adjustment_number)|`int` Readonly||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
|[Void_Time](#void_time)|`datetime` Readonly||
|[Void_User](#void_user)|`nvarchar` Readonly||
|[Adjustment_Time](#adjustment_time)|`datetime` Readonly||
|[Adjustment_User](#adjustment_user)|`nvarchar` Readonly||
|[Read_Only](#read_only)|`bit` Readonly||
|[Notes](#notes)|`nvarchar` ||
|[Document_Version](#document_version)|`int` Readonly||
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` ||
|[Void_Reason](#void_reason)|`nvarchar` Readonly||
|[Reverse_Of_Document_Id](#reverse_of_document_id)|`uniqueidentifier` Readonly||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Planning_Only](#planning_only)|`bit` Readonly||
|[Prime_Cause_Document_Id](#prime_cause_document_id)|`uniqueidentifier` ||
|[Release_Time](#release_time)|`datetime` Readonly||
|[Complete_Time](#complete_time)|`datetime` Readonly||
|[Parent_Document_Relationship_Type](#parent_document_relationship_type)|`nvarchar` Allowed: `S`, `N`, Readonly||
|[Reference_Document_No](#reference_document_no)|`nvarchar` ||
|[User_Status_Id](#user_status_id)|`uniqueidentifier` Readonly||
|[From_Company_Division_Id](#from_company_division_id)|`uniqueidentifier` ||
|[To_Company_Division_Id](#to_company_division_id)|`uniqueidentifier` ||
|[Entity_Name](#entity_name)|`nvarchar` |The entity name of the document header.|
|[Row_Version](#row_version)|`timestamp` ||
|[Asset_Id](#asset_id)|`uniqueidentifier` ||
|[Valuation_Model_Id](#valuation_model_id)|`uniqueidentifier` ||
|[Operation_Type](#operation_type)|`nvarchar` Allowed: `ADJ`, `DEP`, `PUR`, `SLS`, `REV`||
|[Purchase_Value](#purchase_value)|`decimal(0, 0)` ||
|[Purchase_Value_Base](#purchase_value_base)|`decimal(0, 0)` ||
|[Depreciation_Value](#depreciation_value)|`decimal(0, 0)` ||
|[Depreciation_Value_Base](#depreciation_value_base)|`decimal(0, 0)` ||
|[Salvage_Value](#salvage_value)|`decimal(0, 0)` ||
|[Salvage_Value_Base](#salvage_value_base)|`decimal(0, 0)` ||
|[Positive_Reserve_Value](#positive_reserve_value)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_Base](#positive_reserve_value_base)|`decimal(0, 0)` ||
|[Negative_Reserve_Value](#negative_reserve_value)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_Base](#negative_reserve_value_base)|`decimal(0, 0)` ||
|[Asset_Transaction_Date](#asset_transaction_date)|`datetime` ||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Asset_Transaction_Line_Id](#asset_transaction_line_id)|`uniqueidentifier` `PK`||
|[Asset_Transaction_Id](#asset_transaction_id)|`uniqueidentifier` ||

## Columns

### From_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Date

| Property | Value |
| - | - |
|Type|date|

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

### To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Version

| Property | Value |
| - | - |
|Type|int|

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Void_Reason

| Property | Value |
| - | - |
|Type|nvarchar|

### Reverse_Of_Document_Id

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

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valuation_Model_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Purchase_Value

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Value_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Asset_Transaction_Date

| Property | Value |
| - | - |
|Type|datetime|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


