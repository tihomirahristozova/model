# Query Log_Logistic_Unit_Contents_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Serial_Code](#serial_code)|`nvarchar` ||
|[Logistic_Unit_Type_Id](#logistic_unit_type_id)|`uniqueidentifier` |The type of the logistic unit. NULL means the type is currently unknown.|
|[Expected_Weight](#expected_weight)|`decimal(0, 0)` |Expected weight in KG. Used for planning purposes. NULL means unknown.|
|[Measured_Weight](#measured_weight)|`decimal(0, 0)` |Actual measured weight of the unit in KG. NULL means unknown.|
|[Cargo_Type_Id](#cargo_type_id)|`uniqueidentifier` |General type of the cargo of the logistic unit. NULL means unknown or N/A.|
|[Logistic_Unit_Notes](#logistic_unit_notes)|`nvarchar` ||
|[Represented_As_Product_Id](#represented_as_product_id)|`uniqueidentifier` |When the logistic unit is also a tradeable item, specifies the product used to trade the unit. The product should uniquely identify only one logistic unit. Note that this is different from a logistic unit containing a single item. NULL means that the unit is not a tradeable item.|
|[Logistic_Unit_Content_Id](#logistic_unit_content_id)|`uniqueidentifier` `PK`||
|[Logistic_Unit_Id](#logistic_unit_id)|`uniqueidentifier` |The containing logistic unit.|
|[Line_No](#line_no)|`int` |Consecutive position within the logistic unit.|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which is contained in the logistic unit.|
|[Quantity](#quantity)|`decimal(0, 0)` |Quantity of the product in the logistic unit. Expressed in the specified measurement unit.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of the quantity.|
|[Standard_Quantity](#standard_quantity)|`decimal(0, 0)` |The quantity, expessed in the standard measurement unit of the product.|
|[Base_Quantity](#base_quantity)|`decimal(0, 0)` |The quantity, expressed in the base measurement category of the product.|
|[Notes](#notes)|`nvarchar` ||
|[Gross_Weight](#gross_weight)|`decimal(0, 0)` |Gross weight in kilograms (kg). NULL means unknown.|
|[Lot_Number](#lot_number)|`nvarchar` |The production lot number. NULL means unknown.|
|[Expiration_Date](#expiration_date)|`date` |Expiration date of the goods. NULL means unknown or N/A.|

## Columns

### Serial_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Logistic_Unit_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Expected_Weight

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Measured_Weight

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Cargo_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Logistic_Unit_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Represented_As_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Logistic_Unit_Content_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Logistic_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Base_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Gross_Weight

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Expiration_Date

| Property | Value |
| - | - |
|Type|date|


