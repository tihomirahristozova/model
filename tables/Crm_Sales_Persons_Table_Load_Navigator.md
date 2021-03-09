# Query Crm_Sales_Persons_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` `PK`||
|[Person_Id](#person_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Sales_Person_Group_Id](#sales_person_group_id)|`uniqueidentifier` ||
|[Contract_Start_Date](#contract_start_date)|`datetime` ||
|[Contract_End_Date](#contract_end_date)|`datetime` ||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Title](#title)|`nvarchar` `ML`||
|[Gender](#gender)|`nvarchar` Allowed: `F`, `M`||
|[Birth_Date](#birth_date)|`datetime` ||
|[Nationality](#nationality)|`uniqueidentifier` ||
|[National_Number](#national_number)|`nvarchar` ||
|[Passport_Number](#passport_number)|`nvarchar` ||
|[Passport_Issuing_Date](#passport_issuing_date)|`datetime` ||
|[Notes](#notes)|`nvarchar` ||
|[Commission_Policy_Id](#commission_policy_id)|`uniqueidentifier` ||
|[Commission_Percent](#commission_percent)|`decimal(0, 0)` ||
|[Party_Code](#party_code)|`nvarchar` ||
|[GLN](#gln)|`nvarchar` ||
|[Parent_Party_Id](#parent_party_id)|`uniqueidentifier` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location, to which the sales person is assigned. The sales person is allowed to sell to other locations, but this is the default location. NULL means that the sales person is not assigned to any enterprise location.|
|[Is_Active](#is_active)|`bit` |Specifies whether the sales person is active and should be included in the list when choosing sales person through drop-downs, lists, etc.|
|[Sales_Person_Group_Id_L1_Name](#sales_person_group_id_l1_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L2_Name](#sales_person_group_id_l2_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L3_Name](#sales_person_group_id_l3_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L4_Name](#sales_person_group_id_l4_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L5_Name](#sales_person_group_id_l5_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L6_Name](#sales_person_group_id_l6_name)|`nvarchar` `ML`||

## Columns

### Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Contract_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Contract_End_Date

| Property | Value |
| - | - |
|Type|datetime|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Title

| Property | Value |
| - | - |
|Type|nvarchar|

### Gender

| Property | Value |
| - | - |
|Type|nvarchar|

### Birth_Date

| Property | Value |
| - | - |
|Type|datetime|

### Nationality

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### National_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Passport_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Passport_Issuing_Date

| Property | Value |
| - | - |
|Type|datetime|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Commission_Policy_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Commission_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Party_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### GLN

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

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


