# Query Log_Logistic_Unit_Specifications_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Serial_Code](#serial_code)|`nvarchar` ||
|[Logistic_Unit_Type_Id](#logistic_unit_type_id)|`uniqueidentifier` |The type of the logistic unit. NULL means the type is currently unknown.|
|[Expected_Weight](#expected_weight)|`decimal(0, 0)` |Expected weight in KG. Used for planning purposes. NULL means unknown.|
|[Measured_Weight](#measured_weight)|`decimal(0, 0)` |Actual measured weight of the unit in KG. NULL means unknown.|
|[Cargo_Type_Id](#cargo_type_id)|`uniqueidentifier` |General type of the cargo of the logistic unit. NULL means unknown or N/A.|
|[Logisic_Unit_Notes](#logisic_unit_notes)|`nvarchar` ||
|[Represented_As_Product_Id](#represented_as_product_id)|`uniqueidentifier` |When the logistic unit is also a tradeable item, specifies the product used to trade the unit. The product should uniquely identify only one logistic unit. Note that this is different from a logistic unit containing a single item. NULL means that the unit is not a tradeable item.|
|[Logistic_Unit_Specification_Id](#logistic_unit_specification_id)|`uniqueidentifier` `PK`||
|[Logistic_Unit_Id](#logistic_unit_id)|`uniqueidentifier` |The logistic unit, which is detailed by this specification.|
|[Code](#code)|`nvarchar` |The code of the specification, unique within the logistic unit. It can contain only alphanumeric characters and cannot contain spaces.|
|[Name](#name)|`nvarchar` `ML`|Multi-language name of the specification. For some processing purposes, the name might be contained within the client implementation and not saved to the database (NULL).|
|[Value](#value)|`nvarchar` |Text value of the specification. If this is GS1 specification, it can contain only numbers and letters and cannot contain spaces.|
|[Notes](#notes)|`nvarchar` ||

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

### Logisic_Unit_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Represented_As_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Logistic_Unit_Specification_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Logistic_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|


