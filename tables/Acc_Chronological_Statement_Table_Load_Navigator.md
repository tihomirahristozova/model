# Query Acc_Chronological_Statement_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Id](#document_id)|`uniqueidentifier` `PK`||
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
|[Voucher_Id](#voucher_id)|`uniqueidentifier` `PK`||
|[Voucher_Line_Id](#voucher_line_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` ||
|[Account_Id](#account_id)|`uniqueidentifier` ||
|[Account_Name](#account_name)|`nvarchar` `ML`||
|[Item_Key](#item_key)|`nvarchar` ||
|[Currency_Id](#currency_id)|`uniqueidentifier` ||
|[Referenced_Document_Id](#referenced_document_id)|`uniqueidentifier` ||
|[Cost_Center_Id](#cost_center_id)|`uniqueidentifier` ||
|[Profit_Center_Id](#profit_center_id)|`uniqueidentifier` ||
|[Line_Type](#line_type)|`int` ||
|[Line_Type_Base](#line_type_base)|`int` ||
|[Start_Balance](#start_balance)|`decimal(0, 0)` ||
|[Debit](#debit)|`decimal(0, 0)` ||
|[Credit](#credit)|`decimal(0, 0)` ||
|[End_Balance](#end_balance)|`decimal(0, 0)` ||
|[Rate_Multiplier](#rate_multiplier)|`decimal(0, 0)` ||
|[Rate_Divisor](#rate_divisor)|`decimal(0, 0)` ||
|[Type](#type)|`nvarchar` Allowed: `MV`, `SB`||
|[Start_Balance_Base](#start_balance_base)|`decimal(0, 0)` ||
|[Debit_Base](#debit_base)|`decimal(0, 0)` ||
|[Credit_Base](#credit_base)|`decimal(0, 0)` ||
|[End_Balance_Base](#end_balance_base)|`decimal(0, 0)` ||
|[Correspondance_No](#correspondance_no)|`int` ||
|[Correspondant_Amount](#correspondant_amount)|`decimal(0, 0)` Readonly||
|[Example_Voucher_Line_Id](#example_voucher_line_id)|`uniqueidentifier` `PK`||
|[Required_Property_1_Id](#required_property_1_id)|`uniqueidentifier` ||
|[Required_Property_1_Value](#required_property_1_value)|`nvarchar` ||
|[Required_Property_1_Value_Id](#required_property_1_value_id)|`uniqueidentifier` ||
|[Required_Property_1_Description](#required_property_1_description)|`nvarchar` `ML`||
|[Required_Property_2_Id](#required_property_2_id)|`uniqueidentifier` ||
|[Required_Property_2_Value](#required_property_2_value)|`nvarchar` ||
|[Required_Property_2_Value_Id](#required_property_2_value_id)|`uniqueidentifier` ||
|[Required_Property_2_Description](#required_property_2_description)|`nvarchar` `ML`||
|[Required_Property_3_Id](#required_property_3_id)|`uniqueidentifier` ||
|[Required_Property_3_Value](#required_property_3_value)|`nvarchar` ||
|[Required_Property_3_Value_Id](#required_property_3_value_id)|`uniqueidentifier` ||
|[Required_Property_3_Description](#required_property_3_description)|`nvarchar` `ML`||
|[Required_Property_4_Id](#required_property_4_id)|`uniqueidentifier` ||
|[Required_Property_4_Value](#required_property_4_value)|`nvarchar` ||
|[Required_Property_4_Value_Id](#required_property_4_value_id)|`uniqueidentifier` ||
|[Required_Property_4_Description](#required_property_4_description)|`nvarchar` `ML`||
|[Required_Property_5_Id](#required_property_5_id)|`uniqueidentifier` ||
|[Required_Property_5_Value](#required_property_5_value)|`nvarchar` ||
|[Required_Property_5_Value_Id](#required_property_5_value_id)|`uniqueidentifier` ||
|[Required_Property_5_Description](#required_property_5_description)|`nvarchar` `ML`||

## Columns

### Document_Id

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

### Voucher_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Voucher_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Account_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Item_Key

| Property | Value |
| - | - |
|Type|nvarchar|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Referenced_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Profit_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Type

| Property | Value |
| - | - |
|Type|int|

### Line_Type_Base

| Property | Value |
| - | - |
|Type|int|

### Start_Balance

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Debit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Credit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### End_Balance

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Rate_Multiplier

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Rate_Divisor

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Start_Balance_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Debit_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Credit_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### End_Balance_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Correspondance_No

| Property | Value |
| - | - |
|Type|int|

### Correspondant_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Example_Voucher_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_1_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_1_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_1_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_1_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_2_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_2_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_2_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_2_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_3_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_3_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_3_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_3_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_4_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_4_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_4_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_4_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_5_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_5_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_5_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_5_Description

| Property | Value |
| - | - |
|Type|nvarchar|


