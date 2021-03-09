# Query Log_Logistic_Units_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Logistic_Unit_Id](#logistic_unit_id)|`uniqueidentifier` `PK`||
|[Serial_Code](#serial_code)|`nvarchar` |Unique serial code of the logistic unit. If GS1 coding is used, this is the SSCC.|
|[Logistic_Unit_Type_Id](#logistic_unit_type_id)|`uniqueidentifier` |The type of the logistic unit. NULL means the type is currently unknown.|
|[Expected_Weight](#expected_weight)|`decimal(0, 0)` |Expected weight in KG. Used for planning purposes. NULL means unknown.|
|[Measured_Weight](#measured_weight)|`decimal(0, 0)` |Actual measured weight of the unit in KG. NULL means unknown.|
|[Cargo_Type_Id](#cargo_type_id)|`uniqueidentifier` |General type of the cargo of the logistic unit. NULL means unknown or N/A.|
|[Notes](#notes)|`nvarchar` ||
|[Represented_As_Product_Id](#represented_as_product_id)|`uniqueidentifier` |When the logistic unit is also a tradeable item, specifies the product used to trade the unit. The product should uniquely identify only one logistic unit. Note that this is different from a logistic unit containing a single item. NULL means that the unit is not a tradeable item.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Logistic_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Represented_As_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


