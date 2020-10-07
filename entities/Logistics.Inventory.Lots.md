# Logistics.Inventory.Lots

Warehouse lots. They contain one row for each specific product, status, production batch and other specific warehousing conditions. Lot status can block certain operations. Entity: Inv_Lots

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.Lots.md#Id) | guid |  
| [Description](Logistics.Inventory.Lots.md#Description) | [MultilanguageString](../data-types/MultilanguageString.md) (nullable) | The description of this Lot. 
| [ExpiryDate](Logistics.Inventory.Lots.md#ExpiryDate) | datetime (nullable) | Expiry date for this lot. 
| [LicenseNo](Logistics.Inventory.Lots.md#LicenseNo) | string (nullable) | The license number for this lot. Null when license number is N/A or unknown. 
| [Number](Logistics.Inventory.Lots.md#Number) | string | The unique number of the Lot. May contain characters, if required. [Required] [Filter(eq;like)] 
| [ProductionBatchId](Logistics.Inventory.Lots.md#ProductionBatchId) | guid (nullable) | Non-null if the production batch is known. Production batches are automatically created for internal production, but can also be used for specifying production batches for purchased goods. [Filter(multi eq)] 
| [PurchaseLotNumber](Logistics.Inventory.Lots.md#PurchaseLotNumber) | string (nullable) | Identification of the purchase lost with which the products from this store lot are received. E.g. the document number of the Receiving order. [Filter(like)] 
| [ReceiptDate](Logistics.Inventory.Lots.md#ReceiptDate) | date (nullable) | The date of the first receipt of products in this lot. [ReadOnly] 
| [Status](Logistics.Inventory.Lots.md#Status) | [Logistics.Inventory.LotsRepository.Status](Logistics.Inventory.Lots.md#Status) | Status of the warehouse lot. Minus statuses describe blocked conditions. -3 blocked for document (sales or service order) -2 blocked for party -1 blocked for inspection 0 free to use. [Required] [Default(0)] [Filter(multi eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [BlockedForDocument](Logistics.Inventory.Lots.md#BlockedForDocument) | [General.Documents](General.Documents.md) (nullable) | If non-null, contains the document for which the lot is blocked. [Filter(multi eq)] |
| [BlockedForParty](Logistics.Inventory.Lots.md#BlockedForParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | Non-null when the warehouse lot is blocked specifically for some party. [Filter(multi eq)] |
| [CertificateDocument](Logistics.Inventory.Lots.md#CertificateDocument) | [General.Documents](General.Documents.md) (nullable) | Document, containing the certificate for this lot. [Filter(multi eq)] |
| [Product](Logistics.Inventory.Lots.md#Product) | [General.Products.Products](General.Products.Products.md) | The product to which the lot is bound. [Required] [Filter(multi eq)] |
| [ReceiptStoreTransaction](Logistics.Inventory.Lots.md#ReceiptStoreTransaction) | [Logistics.Inventory.StoreTransactions](Logistics.Inventory.StoreTransactions.md) (nullable) | The store receipt transaction, which created the lot. null if the lot is manually created. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Description

> The description of this Lot.

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ExpiryDate

> Expiry date for this lot.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LicenseNo

> The license number for this lot. Null when license number is N/A or unknown.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Number

> The unique number of the Lot. May contain characters, if required. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ProductionBatchId

> Non-null if the production batch is known. Production batches are automatically created for internal production, but can also be used for specifying production batches for purchased goods. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchaseLotNumber

> Identification of the purchase lost with which the products from this store lot are received. E.g. the document number of the Receiving order. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ReceiptDate

> The date of the first receipt of products in this lot. [ReadOnly]

_Type_: **date (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Status

> Status of the warehouse lot. Minus statuses describe blocked conditions. -3 blocked for document (sales or service order) -2 blocked for party -1 blocked for inspection 0 free to use. [Required] [Default(0)] [Filter(multi eq)]

_Type_: **[Logistics.Inventory.LotsRepository.Status](Logistics.Inventory.Lots.md#Status)**  
Allowed values for the [Status](Logistics.Inventory.Lots.md#Status) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| FreeToUse | FreeToUse value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'FreeToUse' |
| BlockedForDocument | BlockedForDocument value. Stored as -3. <br /> _Database Value:_ -3 <br /> _Model Value:_ -3 <br /> _Domain API Value:_ 'BlockedForDocument' |
| BlockedForParty | BlockedForParty value. Stored as -2. <br /> _Database Value:_ -2 <br /> _Model Value:_ -2 <br /> _Domain API Value:_ 'BlockedForParty' |
| BlockedForInspection | BlockedForInspection value. Stored as -1. <br /> _Database Value:_ -1 <br /> _Model Value:_ -1 <br /> _Domain API Value:_ 'BlockedForInspection' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### BlockedForDocument

> If non-null, contains the document for which the lot is blocked. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### BlockedForParty

> Non-null when the warehouse lot is blocked specifically for some party. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### CertificateDocument

> Document, containing the certificate for this lot. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The product to which the lot is bound. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ReceiptStoreTransaction

> The store receipt transaction, which created the lot. null if the lot is manually created. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreTransactions](Logistics.Inventory.StoreTransactions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.Lots erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.Lots erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.Lots erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_Lots?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_Lots?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Inv_Lots?$top=10>

