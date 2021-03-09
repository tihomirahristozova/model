# Query Crm_Sales_Person_Target_Fulfillment_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[From_Party_Id](#from_party_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Document_No](#document_no)|`nvarchar` ||
|[Document_Date](#document_date)|`date` ||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[To_Party_Id](#to_party_id)|`uniqueidentifier` ||
|[Read_Only](#read_only)|`bit` Readonly||
|[Notes](#notes)|`nvarchar` ||
|[Void](#void)|`bit` Readonly||
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` ||
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` ||
|[Adjustment_Number](#adjustment_number)|`int` Readonly||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
|[Void_Time](#void_time)|`datetime` Readonly||
|[Void_User](#void_user)|`nvarchar` Readonly||
|[Sales_Person_Target_Id](#sales_person_target_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Sales_Person_Group_Id](#sales_person_group_id)|`uniqueidentifier` ||
|[Sales_Person_Target_Line_Id](#sales_person_target_line_id)|`uniqueidentifier` `PK`||
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` ||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Period_Month](#period_month)|`tinyint` ||
|[Period_Year](#period_year)|`smallint` ||
|[Target_Amount_Currency_Id](#target_amount_currency_id)|`uniqueidentifier` ||
|[Period_Date](#period_date)|`datetime` ||
|[Target_Type](#target_type)|`nvarchar` Allowed: `SALES`, `BONUS`, `PROMO`, `LOCNT`||
|[Target_Value](#target_value)|`decimal(0, 0)` ||
|[Target_Weight](#target_weight)|`decimal(0, 0)` ||
|[Bonus_Program_Id](#bonus_program_id)|`uniqueidentifier` ||
|[Promotional_Package_Id](#promotional_package_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Target_Amount_Base](#target_amount_base)|`decimal(0, 0)` ||
|[Fulfillment_Amount_Base](#fulfillment_amount_base)|`decimal(0, 0)` ||
|[Base_Currency_Id](#base_currency_id)|`uniqueidentifier` ||
|[Sales_Person_Group_Id_L1_Name](#sales_person_group_id_l1_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L2_Name](#sales_person_group_id_l2_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L3_Name](#sales_person_group_id_l3_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L4_Name](#sales_person_group_id_l4_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L5_Name](#sales_person_group_id_l5_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L6_Name](#sales_person_group_id_l6_name)|`nvarchar` `ML`||
|[Product_Group_Id_L1_Name](#product_group_id_l1_name)|`nvarchar` `ML`||
|[Product_Group_Id_L2_Name](#product_group_id_l2_name)|`nvarchar` `ML`||
|[Product_Group_Id_L3_Name](#product_group_id_l3_name)|`nvarchar` `ML`||
|[Product_Group_Id_L4_Name](#product_group_id_l4_name)|`nvarchar` `ML`||
|[Product_Group_Id_L5_Name](#product_group_id_l5_name)|`nvarchar` `ML`||
|[Product_Group_Id_L6_Name](#product_group_id_l6_name)|`nvarchar` `ML`||

## Columns

### From_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

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

### State

| Property | Value |
| - | - |
|Type|smallint|

### To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Read_Only

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Void

| Property | Value |
| - | - |
|Type|bit|

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

### Sales_Person_Target_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Target_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Period_Month

| Property | Value |
| - | - |
|Type|tinyint|

### Period_Year

| Property | Value |
| - | - |
|Type|smallint|

### Target_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Period_Date

| Property | Value |
| - | - |
|Type|datetime|

### Target_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Value

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Target_Weight

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Bonus_Program_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Promotional_Package_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Target_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Fulfillment_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Base_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


