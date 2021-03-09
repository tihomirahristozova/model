# Query Its_Declaration_Lines_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
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
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` Readonly||
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
|[Intrastat_Declaration_Id](#intrastat_declaration_id)|`uniqueidentifier` `PK`|Intrastat declaration id|
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Reference_Year](#reference_year)|`smallint` ||
|[Reference_Month](#reference_month)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `10`, `11`, `12`||
|[Goods_Flow_Direction](#goods_flow_direction)|`nvarchar` Allowed: `A`, `D`||
|[Declaration_Function](#declaration_function)|`nvarchar` Allowed: `R`, `C`||
|[Declare_Statistical_Values](#declare_statistical_values)|`bit` ||
|[Postal_Code](#postal_code)|`nvarchar` ||
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Third_Declaring_Party_Id](#third_declaring_party_id)|`uniqueidentifier` |Third declaring party, which holds the electronic signature. This is the company which submits the declaration.|
|[Authorized_Person_Id](#authorized_person_id)|`uniqueidentifier` |The authorized person who submits the intrastat declaration.|
|[Intrastat_Declaration_Line_Id](#intrastat_declaration_line_id)|`uniqueidentifier` `PK`||
|[Line_No](#line_no)|`int` ||
|[Intrastat_Commodity_Code_Id](#intrastat_commodity_code_id)|`uniqueidentifier` ||
|[Origin_Country_Id](#origin_country_id)|`uniqueidentifier` ||
|[Party_Country_Id](#party_country_id)|`uniqueidentifier` ||
|[Transport_Country_Id](#transport_country_id)|`uniqueidentifier` ||
|[Transaction_Nature](#transaction_nature)|`nvarchar` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`||
|[Transport_Mode](#transport_mode)|`nvarchar` Allowed: `1`, `2`, `3`, `4`, `5`, `7`, `8`, `9`||
|[Delivery_Terms](#delivery_terms)|`nvarchar` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`||
|[Administrative_Region_Id](#administrative_region_id)|`uniqueidentifier` ||
|[Net_Mass_Kg](#net_mass_kg)|`decimal(0, 0)` ||
|[Invoiced_Value_Amount_Base](#invoiced_value_amount_base)|`decimal(0, 0)` ||
|[Statistical_Value_Amount_Base](#statistical_value_amount_base)|`decimal(0, 0)` ||
|[Quantity_Supplementary_Unit](#quantity_supplementary_unit)|`decimal(0, 0)` ||
|[Line_Action](#line_action)|`nvarchar` Allowed: `NEW`, `EDN`, `EDO`, `DEL`||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Intrastat_Declaration_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reference_Year

| Property | Value |
| - | - |
|Type|smallint|

### Reference_Month

| Property | Value |
| - | - |
|Type|tinyint|

### Goods_Flow_Direction

| Property | Value |
| - | - |
|Type|nvarchar|

### Declaration_Function

| Property | Value |
| - | - |
|Type|nvarchar|

### Declare_Statistical_Values

| Property | Value |
| - | - |
|Type|bit|

### Postal_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Third_Declaring_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Authorized_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Intrastat_Declaration_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Intrastat_Commodity_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Origin_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transport_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Nature

| Property | Value |
| - | - |
|Type|nvarchar|

### Transport_Mode

| Property | Value |
| - | - |
|Type|nvarchar|

### Delivery_Terms

| Property | Value |
| - | - |
|Type|nvarchar|

### Administrative_Region_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Net_Mass_Kg

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Invoiced_Value_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Statistical_Value_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Supplementary_Unit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Action

| Property | Value |
| - | - |
|Type|nvarchar|


