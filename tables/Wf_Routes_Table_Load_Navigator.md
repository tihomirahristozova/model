# Query Wf_Routes_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Route_Id](#route_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Process_Event](#process_event)|`nvarchar` ||
|[Condition_States_Bit_Mask](#condition_states_bit_mask)|`int` ||
|[Condition_Filter_XML](#condition_filter_xml)|`nvarchar` ||
|[Procedure_Name](#procedure_name)|`nvarchar` ||
|[Destination_Document_Type_Id](#destination_document_type_id)|`uniqueidentifier` ||
|[Activation_Date](#activation_date)|`date` ||
|[Deactivation_Date](#deactivation_date)|`date` ||
|[Notes](#notes)|`nvarchar` ||
|[Active](#active)|`bit` ||
|[Destination_State](#destination_state)|`smallint` Allowed: `0`, `10`, `20`, `30`, `40`, `50`||
|[Read_Only](#read_only)|`bit` ||
|[Schema_XML](#schema_xml)|`nvarchar` ||
|[Condition_Enterprise_Company_Id](#condition_enterprise_company_id)|`uniqueidentifier` ||
|[Destination_Enterprise_Company_Id](#destination_enterprise_company_id)|`uniqueidentifier` ||
|[Allowed_Generation_Types](#allowed_generation_types)|`nvarchar` Allowed: `A`, `B`, `M`||
|[Allow_Obsolete_Generation](#allow_obsolete_generation)|`bit` ||
|[Connected_Party_Condition](#connected_party_condition)|`nvarchar` Allowed: `A`, `C`, `U`||
|[Parent_Document_Relationship_Type](#parent_document_relationship_type)|`nvarchar` Allowed: `S`, `N`||
|[Destination_Enterprise_Company_Location_Id](#destination_enterprise_company_location_id)|`uniqueidentifier` ||
|[Condition_User_Status_Id](#condition_user_status_id)|`uniqueidentifier` ||
|[Destination_User_Status_Id](#destination_user_status_id)|`uniqueidentifier` ||
|[Negative_Condition_Filter_Xml](#negative_condition_filter_xml)|`nvarchar` |The negative condition should NOT be matched by the document in order to execute the route.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Route_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Event

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_States_Bit_Mask

| Property | Value |
| - | - |
|Type|int|

### Condition_Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar|

### Procedure_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Destination_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Activation_Date

| Property | Value |
| - | - |
|Type|date|

### Deactivation_Date

| Property | Value |
| - | - |
|Type|date|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Destination_State

| Property | Value |
| - | - |
|Type|smallint|

### Read_Only

| Property | Value |
| - | - |
|Type|bit|

### Schema_XML

| Property | Value |
| - | - |
|Type|nvarchar|

### Condition_Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Destination_Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Allowed_Generation_Types

| Property | Value |
| - | - |
|Type|nvarchar|

### Allow_Obsolete_Generation

| Property | Value |
| - | - |
|Type|bit|

### Connected_Party_Condition

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Document_Relationship_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Destination_Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Destination_User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Negative_Condition_Filter_Xml

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


