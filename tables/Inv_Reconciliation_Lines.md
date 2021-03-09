# Table Inv_Reconciliation_Lines

Store reconciliations (physical counting) detail lines. Each line contains the reconciliation for one combination of product, lot, bin and serial number. Entity: Inv_Reconciliation_Lines

## Owner Tables Hierarchy

* [Inv_Reconciliations](Inv_Reconciliations.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Ord](#line_ord)|`int` |The ordinal position of the line within the document. Duplicates are allowed, but not suggested|
|[Store_Id](#store_id)|`uniqueidentifier` |The store, containing the reconciled product|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |The store bin, that was counted|
|[Product_Id](#product_id)|`uniqueidentifier` |The id of the reconciled product|
|[Quantity](#quantity)|`decimal(18, 3)` |Quantity found at the reconciliation, |
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Quantity_Base](#quantity_base)|`decimal(18, 3)` |Quantity found at the reconciliation, expressed in base measurement units|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The lot, which was reconciled.|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Item serial number for serialized items. NULL for non-serializable items|
|[Available_Quantity_Base](#available_quantity_base)|`decimal(18, 3)` Readonly|Quantity found at the reconciliation, in the base measurement category of the product.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Reconciliation_Id](#reconciliation_id)|`uniqueidentifier` |Parent reconciliation Id|
|[Reconciliation_Line_Id](#reconciliation_line_id)|`uniqueidentifier` `PK`|Unique line Id|
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` |Exact time when the transaction occurred|
|[Row_Version](#row_version)|`timestamp` ||
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |Selects the product thru some of the product codes.|
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

## Columns

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Id

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

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Available_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Reconciliation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reconciliation_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|


