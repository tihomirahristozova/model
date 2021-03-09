# Query Gen_Areas_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Area_Id](#area_id)|`uniqueidentifier` `PK`||
|[Area_Name](#area_name)|`nvarchar` `ML`||
|[Area_Code](#area_code)|`nvarchar` ||
|[Parent_Area_Id](#parent_area_id)|`uniqueidentifier` |Parent area in the hierarchy.|
|[Full_Path](#full_path)|`nvarchar` Readonly|Full path to the area, starting with '/' and containing the area codes of all parent areas using '/' as separator and terminator. For example root area with code 'BG' would have full path = '/BG/'|
|[Parent_Area_Id_L1_Name](#parent_area_id_l1_name)|`nvarchar` `ML`||
|[Parent_Area_Id_L2_Name](#parent_area_id_l2_name)|`nvarchar` `ML`||
|[Parent_Area_Id_L3_Name](#parent_area_id_l3_name)|`nvarchar` `ML`||
|[Parent_Area_Id_L4_Name](#parent_area_id_l4_name)|`nvarchar` `ML`||
|[Parent_Area_Id_L5_Name](#parent_area_id_l5_name)|`nvarchar` `ML`||
|[Parent_Area_Id_L6_Name](#parent_area_id_l6_name)|`nvarchar` `ML`||

## Columns

### Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Area_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Full_Path

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Area_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Area_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Area_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Area_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Area_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Area_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


