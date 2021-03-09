# Query Pos_Locations_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Pos_Location_Id](#pos_location_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company of the POS location.|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location of the POS location. Currently, only one POS location is allowed for each company location.|
|[Pos_Location_Code](#pos_location_code)|`nvarchar` |Unique (with the enterprise company) code of this POS location.|
|[Is_Active](#is_active)|`bit` |Indicates whether the POS location is currently active and can be chosen in drop-downs, etc.|
|[Party_Id](#party_id)|`uniqueidentifier` |The party of the company location.|
|[Company_Id](#company_id)|`uniqueidentifier` |The company to which this location belongs.|
|[Location_Name](#location_name)|`nvarchar` `ML`|The name of the company location.|
|[Working_Time](#working_time)|`nvarchar` |Textual representation of the working time of the location.|
|[Bill_To](#bill_to)|`nvarchar` Allowed: `C`, `L`|If filled indicates which party is billed for the amounts from documents that require payments. This setting is used in CRM module when the company and the location are customers. Possible values: 'C' = Company, 'L' = Company location, NULL = unidentified|
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` ||
|[Notes](#notes)|`nvarchar` ||
|[Parent_Party_Id](#parent_party_id)|`uniqueidentifier` |Organizational unit (branch from the hierarchy of all parties) to which this party is referred to|
|[Area_Id](#area_id)|`uniqueidentifier` |The area in which the party is situated.|
|[Default_Product_Coding_System_Id](#default_product_coding_system_id)|`uniqueidentifier` |When not null, specifies coding system for products, which is required by the party. The coding system is used primarily for document printouts and document import/exports.|
|[Party_Is_Active](#party_is_active)|`bit` |Specifies whether the current party is active in the system or not.|
|[Area_Id_L1_Name](#area_id_l1_name)|`nvarchar` `ML`||
|[Area_Id_L2_Name](#area_id_l2_name)|`nvarchar` `ML`||
|[Area_Id_L3_Name](#area_id_l3_name)|`nvarchar` `ML`||
|[Area_Id_L4_Name](#area_id_l4_name)|`nvarchar` `ML`||
|[Area_Id_L5_Name](#area_id_l5_name)|`nvarchar` `ML`||
|[Area_Id_L6_Name](#area_id_l6_name)|`nvarchar` `ML`||

## Columns

### Pos_Location_Id

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

### Pos_Location_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Location_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Working_Time

| Property | Value |
| - | - |
|Type|nvarchar|

### Bill_To

| Property | Value |
| - | - |
|Type|nvarchar|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Product_Coding_System_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Area_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


