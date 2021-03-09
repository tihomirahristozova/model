# Table Srv_Service_Invoicing

Contains invoicing ratios for the listed services. Entity: Srv_Service_Invoicing

## Owner Tables Hierarchy

* [Srv_Services](Srv_Services.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Service_Invoicing_Id](#service_invoicing_id)|`uniqueidentifier` `PK`||
|[Service_Id](#service_id)|`uniqueidentifier` |The service for which the invoicing instructions are|
|[Quantity_Of_Service](#quantity_of_service)|`decimal(18, 3)` |The quantity of service for which the invoicing is specified|
|[Product_Id](#product_id)|`uniqueidentifier` |The product that should be invoiced|
|[Quantity_Of_Product](#quantity_of_product)|`decimal(18, 3)` |The quantity to invoice|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Service_Invoicing_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Of_Service

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Of_Product

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


