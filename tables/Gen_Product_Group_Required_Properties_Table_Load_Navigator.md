# Query Gen_Product_Group_Required_Properties_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Required_Property_Id](#required_property_id)|`uniqueidentifier` `PK`||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Property_No](#property_no)|`int` |The consecutive number (position) of the property within the product group and its subgroups. The parent groups of each leaf group should contain only unique property numbers.|
|[Property_Id](#property_id)|`uniqueidentifier` ||
|[Default_Property_Value](#default_property_value)|`nvarchar` ||
|[Default_Property_Value_Description](#default_property_value_description)|`nvarchar` ||
|[Default_Value_Id](#default_value_id)|`uniqueidentifier` |When not null, specifies the default internal Id value of the property, for new products in the group.|
|[Required](#required)|`bit` |Specifies whether the property is required (or only suggested) to be set for new products. Suggested properties are used by product configuration and other product creation services. 1=Required, 0=Suggested.|
|[Row_Version](#row_version)|`timestamp` ||
|[Product_Group_Id_L1_Name](#product_group_id_l1_name)|`nvarchar` `ML`||
|[Product_Group_Id_L2_Name](#product_group_id_l2_name)|`nvarchar` `ML`||
|[Product_Group_Id_L3_Name](#product_group_id_l3_name)|`nvarchar` `ML`||
|[Product_Group_Id_L4_Name](#product_group_id_l4_name)|`nvarchar` `ML`||
|[Product_Group_Id_L5_Name](#product_group_id_l5_name)|`nvarchar` `ML`||
|[Product_Group_Id_L6_Name](#product_group_id_l6_name)|`nvarchar` `ML`||

## Columns

### Required_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Property_No

| Property | Value |
| - | - |
|Type|int|

### Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Property_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Default_Property_Value_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Default_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

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


