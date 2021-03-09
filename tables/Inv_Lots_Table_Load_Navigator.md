# Query Inv_Lots_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Lot_Id](#lot_id)|`uniqueidentifier` `PK`||
|[Lot_Number](#lot_number)|`nvarchar` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Receipt_Store_Transaction_Id](#receipt_store_transaction_id)|`uniqueidentifier` ||
|[Production_Batch_Id](#production_batch_id)|`uniqueidentifier` ||
|[Status](#status)|`int` Allowed: `0`, `-1`, `-2`, `-3`||
|[Blocked_For_Party_Id](#blocked_for_party_id)|`uniqueidentifier` ||
|[Blocked_For_Document_Id](#blocked_for_document_id)|`uniqueidentifier` ||
|[Expiry_Date](#expiry_date)|`datetime` ||
|[License_No](#license_no)|`nvarchar` ||
|[Description](#description)|`nvarchar` `ML`||
|[Purchase_Lot_Number](#purchase_lot_number)|`nvarchar` ||
|[Receipt_Date](#receipt_date)|`date` Readonly||
|[Row_Version](#row_version)|`timestamp` ||
|[Certificate_Document_Id](#certificate_document_id)|`uniqueidentifier` ||
|[Excise_Measuring_Transaction_Id](#excise_measuring_transaction_id)|`uniqueidentifier` |When the lot was created in an excise controlled environment, specifies the measuring transaction which was used to create the lot.|

## Columns

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receipt_Store_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Production_Batch_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Status

| Property | Value |
| - | - |
|Type|int|

### Blocked_For_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Blocked_For_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Expiry_Date

| Property | Value |
| - | - |
|Type|datetime|

### License_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Purchase_Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Receipt_Date

| Property | Value |
| - | - |
|Type|date|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Certificate_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Excise_Measuring_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


