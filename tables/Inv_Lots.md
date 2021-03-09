# Table Inv_Lots

Warehouse lots. They contain one row for each specific product, status, production batch and other specific warehousing conditions. Lot status can block certain operations. Entity: Inv_Lots

## Summary

| Name | Type | Description |
| - | - | --- |
|[Lot_Id](#lot_id)|`uniqueidentifier` `PK`||
|[Lot_Number](#lot_number)|`nvarchar(30)` ||
|[Product_Id](#product_id)|`uniqueidentifier` |The product to which the lot is bound|
|[Receipt_Store_Transaction_Id](#receipt_store_transaction_id)|`uniqueidentifier` |The store receipt transaction, which created the lot. NULL if the lot is manually created|
|[Production_Batch_Id](#production_batch_id)|`uniqueidentifier` |Non-NULL if the production batch is known. Production batches are automatically created for internal production, but can also be used for specifying production batches for purchased goods|
|[Status](#status)|`int` Allowed: `0`, `-1`, `-2`, `-3`|Status of the warehouse lot. Minus statuses describe blocked conditions.
-3 blocked for document (sales or service order)
-2 blocked for party
-1 blocked for inspection
0 free to use|
|[Blocked_For_Party_Id](#blocked_for_party_id)|`uniqueidentifier` |Non-NULL when the warehouse lot is blocked specifically for some party|
|[Blocked_For_Document_Id](#blocked_for_document_id)|`uniqueidentifier` |If non-null, contains the document for which the lot is blocked|
|[Expiry_Date](#expiry_date)|`datetime` ||
|[License_No](#license_no)|`nvarchar(50)` |The license number for this lot. Null when license number is N/A or unknown.|
|[Description](#description)|`nvarchar(254)` `ML`||
|[Purchase_Lot_Number](#purchase_lot_number)|`nvarchar(30)` |Identification of the purchase lost with which the products from this store lot are received. E.g. the document number of the Receiving order.|
|[Receipt_Date](#receipt_date)|`date` Readonly|The date of the first receipt of products in this lot.|
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
|Type|nvarchar(30)|

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
|Type|nvarchar(50)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Purchase_Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar(30)|

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


