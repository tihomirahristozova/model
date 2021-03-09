# Table Srv_Service_Objects

Contains the serviceable objects. The service objects can be covered by service agreements, serviced in service activities, etc. Entity: Srv_Service_Objects

## Summary

| Name | Type | Description |
| - | - | --- |
|[Service_Object_Id](#service_object_id)|`uniqueidentifier` `PK`||
|[Service_Object_Name](#service_object_name)|`nvarchar(254)` ||
|[Serial_Number](#serial_number)|`nvarchar(32)` |The serial number of the item, that is being serviced|
|[Service_Object_Type_Id](#service_object_type_id)|`uniqueidentifier` |When not NULL specifies the type of the service object|
|[Product_Id](#product_id)|`uniqueidentifier` |When not-NULL identifies the product, from which the service object was created|
|[Notes](#notes)|`nvarchar(254)` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Serial number for the product, that corresponds to this service object. If there is no product, then the other field for 'Serial number' is used to specify this data.|
|[Serviced_Product_Id](#serviced_product_id)|`uniqueidentifier` |The product, which is used to physically store the service object, when it is serviced. Need to be specified, only when it is different from Product; otherwise, it is null.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Service_Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Object_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Serial_Number

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Service_Object_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serviced_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


