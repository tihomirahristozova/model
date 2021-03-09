# Procedure Inv_Reconciliations_Table_Printout_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Ord](#line_ord)|`int` |The ordinal position of the line within the document. Duplicates are allowed, but not suggested|
|[Reconciliation_Line_Id](#reconciliation_line_id)|`uniqueidentifier` `PK`|Unique line Id|
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` |Exact time when the transaction occurred|
|[Base_Measurement_Unit_Name](#base_measurement_unit_name)|`nvarchar` ||
|[Current_Available_Quantity_Base](#current_available_quantity_base)|`decimal(0, 0)` ||
|[Quantity_Base](#quantity_base)|`decimal(18, 3)` |Quantity found at the reconciliation, expressed in base measurement units|
|[Quantity_Unit_Id_Text](#quantity_unit_id_text)|`nvarchar` `ML`||
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Quantity](#quantity)|`decimal(18, 3)` |Quantity found at the reconciliation, |
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Item serial number for serialized items. NULL for non-serializable items|
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Product_Id_Text](#product_id_text)|`nvarchar` ||
|[Product_Id](#product_id)|`uniqueidentifier` |The id of the reconciled product|
|[Store_Bin_Id_Text](#store_bin_id_text)|`nvarchar` `ML`||
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |The store bin, that was counted|
|[Store_Id_Text](#store_id_text)|`nvarchar` `ML`||
|[Store_Id](#store_id)|`uniqueidentifier` |The store, containing the reconciled product|
|[Reconciliation_Id](#reconciliation_id)|`uniqueidentifier` |Parent reconciliation Id|
|[Available_Quantity_Base](#available_quantity_base)|`decimal(18, 3)` Readonly|Quantity found at the reconciliation, in the base measurement category of the product.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The lot, which was reconciled.|

## Columns

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Reconciliation_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### Base_Measurement_Unit_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Current_Available_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Quantity_Unit_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reconciliation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Available_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


