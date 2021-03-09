# Query Prd_Material_Consumption_Report_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Id](#id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Document_No](#document_no)|`nvarchar` ||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[Store_Id](#store_id)|`uniqueidentifier` |The store from which to retrieve the material.|
|[Document_Date](#document_date)|`date` ||
|[Work_Order_Id](#work_order_id)|`uniqueidentifier` `PK`||
|[Work_Order_Item_Id](#work_order_item_id)|`uniqueidentifier` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Material_Id](#material_id)|`uniqueidentifier` ||
|[Material_Name](#material_name)|`nvarchar` `ML`||
|[Work_Order_Item_Operation_Id](#work_order_item_operation_id)|`uniqueidentifier` ||
|[Operation_Description](#operation_description)|`nvarchar` ||
|[Planned_Quantity](#planned_quantity)|`decimal(0, 0)` ||
|[Invested_Quantity](#invested_quantity)|`decimal(0, 0)` ||
|[Setup_Quantity](#setup_quantity)|`decimal(0, 0)` ||
|[Run_Quantity](#run_quantity)|`decimal(0, 0)` ||
|[Scrap_Quantity](#scrap_quantity)|`decimal(0, 0)` ||
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` ||
|[Output_Store_Id](#output_store_id)|`uniqueidentifier` |Output store for the production|

## Columns

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Id

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

### State

| Property | Value |
| - | - |
|Type|smallint|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### Work_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Material_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Material_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Work_Order_Item_Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Planned_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Invested_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Setup_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Run_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Scrap_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Output_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


