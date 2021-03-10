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


Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Inv_Lots](Inv_Lots.md).[Lot_Id](Inv_Lots.md#lot_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Lot_Number


Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar(30)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Lot_Number](Inv_Lots.md#lot_number)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|30|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|yes|

### Product_Id


Product_Id


The product to which the lot is bound


The product to which the lot is bound

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Product_Id](Inv_Lots.md#product_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Receipt_Store_Transaction_Id


Receipt_Store_Transaction_Id


The store receipt transaction, which created the lot. NULL if the lot is manually created


The store receipt transaction, which created the lot. NULL if the lot is manually created

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Transactions](Inv_Transactions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Receipt_Store_Transaction_Id](Inv_Lots.md#receipt_store_transaction_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Production_Batch_Id


Production_Batch_Id


Non-NULL if the production batch is known. Production batches are automatically created for internal production, but can also be used for specifying production batches for purchased goods


Non-NULL if the production batch is known. Production batches are automatically created for internal production, but can also be used for specifying production batches for purchased goods

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Production_Batch_Id](Inv_Lots.md#production_batch_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Status


Status


Status of the warehouse lot. Minus statuses describe blocked conditions.
-3 blocked for document (sales or service order)
-2 blocked for party
-1 blocked for inspection
0 free to use


Status of the warehouse lot. Minus statuses describe blocked conditions.
-3 blocked for document (sales or service order)
-2 blocked for party
-1 blocked for inspection
0 free to use

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`0`, `-1`, `-2`, `-3`|
|Default Value|0|
|Derived From|[Inv_Lots](Inv_Lots.md).[Status](Inv_Lots.md#status)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Blocked_For_Party_Id


Blocked_For_Party_Id


Non-NULL when the warehouse lot is blocked specifically for some party


Non-NULL when the warehouse lot is blocked specifically for some party

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Blocked_For_Party_Id](Inv_Lots.md#blocked_for_party_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Blocked_For_Document_Id


Blocked_For_Document_Id


If non-null, contains the document for which the lot is blocked


If non-null, contains the document for which the lot is blocked

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Blocked_For_Document_Id](Inv_Lots.md#blocked_for_document_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Expiry_Date


Expiry_Date

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Expiry_Date](Inv_Lots.md#expiry_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### License_No


License_No


The license number for this lot. Null when license number is N/A or unknown.


The license number for this lot. Null when license number is N/A or unknown.

| Property | Value |
| - | - |
|Type|nvarchar(50)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[License_No](Inv_Lots.md#license_no)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|50|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Description


Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Description](Inv_Lots.md#description)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Purchase_Lot_Number


Purchase_Lot_Number


Identification of the purchase lost with which the products from this store lot are received. E.g. the document number of the Receiving order.


Identification of the purchase lost with which the products from this store lot are received. E.g. the document number of the Receiving order.

| Property | Value |
| - | - |
|Type|nvarchar(30)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Purchase_Lot_Number](Inv_Lots.md#purchase_lot_number)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|30|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Receipt_Date


Receipt_Date


The date of the first receipt of products in this lot.


The date of the first receipt of products in this lot.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Receipt_Date](Inv_Lots.md#receipt_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Row_Version](Inv_Lots.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Certificate_Document_Id


Certificate_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Certificate_Document_Id](Inv_Lots.md#certificate_document_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Excise_Measuring_Transaction_Id


Excise_Measuring_Transaction_Id


When the lot was created in an excise controlled environment, specifies the measuring transaction which was used to create the lot.


When the lot was created in an excise controlled environment, specifies the measuring transaction which was used to create the lot.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Exc_Measuring_Transactions](Exc_Measuring_Transactions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Lots](Inv_Lots.md).[Excise_Measuring_Transaction_Id](Inv_Lots.md#excise_measuring_transaction_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|


