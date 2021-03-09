# Table Prd_Production_Schedule


## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The document Id of the base order for this MPS entry|
|[Workgroup_Id](#workgroup_id)|`uniqueidentifier` |The workgroup, which is scheduled|
|[Product_Id](#product_id)|`uniqueidentifier` |The item that is scheduled for production|
|[Quantity](#quantity)|`decimal(18, 3)` |The quantity that should be produced|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Need_Date](#need_date)|`datetime` |The date, when the item should be ready for shipment|
|[Notes](#notes)|`nvarchar(254)` |Short note from the scheduler|
|[Customer_Name_Temp](#customer_name_temp)|`nvarchar(64)` ||
|[Order_Number_Temp](#order_number_temp)|`nvarchar(16)` ||
|[Order_Date_Temp](#order_date_temp)|`datetime` ||
|[Status](#status)|`nvarchar(1)` |P=Planned; R=Released to manufacturing (e.g. history record)|
|[Schedule_Basis](#schedule_basis)|`nvarchar(1)` |M=MPS; F=FAS|
|[Store_Id](#store_id)|`uniqueidentifier` |The store where the product must be finished|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Workgroup_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Need_Date

| Property | Value |
| - | - |
|Type|datetime|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Customer_Name_Temp

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Order_Number_Temp

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Order_Date_Temp

| Property | Value |
| - | - |
|Type|datetime|

### Status

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Schedule_Basis

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


