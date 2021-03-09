# Table Crm_Discount_Types

Contains the different types of discounts, which can be applied to sales lines. Different types of discounts can be combined for a single sales line. Entity: Crm_Discount_Types

## Summary

| Name | Type | Description |
| - | - | --- |
|[Discount_Type_Id](#discount_type_id)|`uniqueidentifier` `PK`||
|[Discount_Type_Code](#discount_type_code)|`nvarchar(32)` ||
|[Discount_Type_Name](#discount_type_name)|`nvarchar(254)` ||
|[Calculation_Method](#calculation_method)|`nvarchar(1)` Allowed: `S`, `P`, `B`|Specifies whether the calculation method of the discount is based on a standard discount, promotional package, bonus program, etc.|
|[Ord](#ord)|`int` |Determines the order in which the discounts are applied. The discounts with smaller Ord are applied first.|
|[Action_Type](#action_type)|`nvarchar(1)` Allowed: `A`, `R`, `M`|Specifies the way the discount is applied over the previous discounts.|
|[Is_System](#is_system)|`bit` |Specifies whether this discount type is created and managed by the system.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Discount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Discount_Type_Code

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Discount_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Calculation_Method

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Ord

| Property | Value |
| - | - |
|Type|int|

### Action_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Is_System

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


