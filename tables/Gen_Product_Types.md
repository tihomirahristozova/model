# Table Gen_Product_Types

Categorization of the products by their nature. Entity: Gen_Product_Types

## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Type_Id](#product_type_id)|`uniqueidentifier` `PK`||
|[Product_Type_Code](#product_type_code)|`nvarchar(16)` ||
|[Product_Type_Name](#product_type_name)|`nvarchar(254)` `ML`||
|[Is_Stocked](#is_stocked)|`bit` |1=The products of this type are stocked in a warehouse; 0=otherwise (services)|
|[Is_Serviced](#is_serviced)|`bit` |1 when the products of this type create service agreements and can be serviced|
|[Is_Fixed_Asset](#is_fixed_asset)|`bit` |1 when assets are acquired or retired when products from this type are purchased or sold|
|[Is_Shipped](#is_shipped)|`bit` |1 when the products from this type are being shipped after sales.|
|[Is_Service_Activity_Service](#is_service_activity_service)|`bit` |1 when the product corresponds to service used in service documents (like service activities)|
|[Is_Default](#is_default)|`bit` |When checked specifies that this type is set by default for new products unless another type is specified in the product groups.|
|[Lot_Auto_Creation](#lot_auto_creation)|`bit` |If checked specifies that lots are automatically created by the receiving orders with which the products are received.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Product_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Type_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Product_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Stocked

| Property | Value |
| - | - |
|Type|bit|

### Is_Serviced

| Property | Value |
| - | - |
|Type|bit|

### Is_Fixed_Asset

| Property | Value |
| - | - |
|Type|bit|

### Is_Shipped

| Property | Value |
| - | - |
|Type|bit|

### Is_Service_Activity_Service

| Property | Value |
| - | - |
|Type|bit|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Lot_Auto_Creation

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


