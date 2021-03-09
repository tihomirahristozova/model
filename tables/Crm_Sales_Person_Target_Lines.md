# Table Crm_Sales_Person_Target_Lines

Detail records (lines) of targets for sales persons. Entity: Crm_Sales_Person_Target_Lines

## Owner Tables Hierarchy

* [Crm_Sales_Person_Targets](Crm_Sales_Person_Targets.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sales_Person_Target_Line_Id](#sales_person_target_line_id)|`uniqueidentifier` `PK`||
|[Sales_Person_Target_Id](#sales_person_target_id)|`uniqueidentifier` ||
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` |Sales person to whom the target is assigned|
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` |Product group for which the target is defined|
|[Period_Month](#period_month)|`tinyint` |Month of the period in which the target must be fulfilled (the period is determined by specifying a month and an year)|
|[Period_Year](#period_year)|`smallint` |Year of the period in which the target must be fulfilled (the period is determined by specifying a month and an year)|
|[Target_Amount](#target_amount)|`decimal(18, 2)` |Target amount to be fulfilled by the specified sales person. Deprecated - use Target_Value|
|[Target_Amount_Currency_Id](#target_amount_currency_id)|`uniqueidentifier` |Deprecated - use currency in document header|
|[Period_Date](#period_date)|`datetime` Readonly|Calculated date representation of the target period (used for grouping, filtering and other auxiliary purposes)|
|[Target_Type](#target_type)|`nvarchar(5)` Allowed: `SALES`, `BONUS`, `PROMO`, `LOCNT`|Type of target. Defines the meaning of Target_Value. SALES-sales amount, BONUS-count of bonus progs, PACK-count of promo packs|
|[Target_Value](#target_value)|`decimal(9, 2)` |Value of target. Meaning depends on target type|
|[Target_Weight](#target_weight)|`decimal(5, 2)` |Relative weight of target, comparatively to other targets|
|[Bonus_Program_Id](#bonus_program_id)|`uniqueidentifier` |Bonus program Id when the target type is BONUS, NULL otherwise|
|[Promotional_Package_Id](#promotional_package_id)|`uniqueidentifier` |Promotional Package Id when the target type is PROMO, NULL otherwise|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sales_Person_Target_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Target_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Period_Month

| Property | Value |
| - | - |
|Type|tinyint|

### Period_Year

| Property | Value |
| - | - |
|Type|smallint|

### Target_Amount

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Target_Amount_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Period_Date

| Property | Value |
| - | - |
|Type|datetime|

### Target_Type

| Property | Value |
| - | - |
|Type|nvarchar(5)|

### Target_Value

| Property | Value |
| - | - |
|Type|decimal(9, 2)|

### Target_Weight

| Property | Value |
| - | - |
|Type|decimal(5, 2)|

### Bonus_Program_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Promotional_Package_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


