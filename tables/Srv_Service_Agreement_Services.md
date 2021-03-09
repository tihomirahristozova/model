# Table Srv_Service_Agreement_Services

Contains the free services, included in the service agreement. Entity: Srv_Service_Agreement_Services

## Owner Tables Hierarchy

* [Srv_Service_Agreements](Srv_Service_Agreements.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc.|
|[Service_Id](#service_id)|`uniqueidentifier` |Paid or agreed in advance service that won't be invoiced after service activities (if Service_Id is filled then Service_Product_Id must be NULL)|
|[Service_Product_Id](#service_product_id)|`uniqueidentifier` |Paid or agreed in advance product that will be substracted from the invoiced products from service activities (if Service_Product_Id is filled then Service_Id must be NULL)|
|[Quantity](#quantity)|`decimal(18, 3)` |Quantity of the agreed servcice or product|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Start_Date](#start_date)|`datetime` |Start date from which the agreedment for the service or product is valid. For the agreement period, the service could be performed free of charge in service activities.|
|[End_Date](#end_date)|`datetime` |End date to which the agreedment for the service or product is valid. For the agreement period, the service could be performed free of charge in service activities.|
|[Service_Agreement_Service_Id](#service_agreement_service_id)|`uniqueidentifier` `PK`||
|[Service_Agreement_Id](#service_agreement_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Service_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Product_Id

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

### Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### End_Date

| Property | Value |
| - | - |
|Type|datetime|

### Service_Agreement_Service_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Agreement_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


