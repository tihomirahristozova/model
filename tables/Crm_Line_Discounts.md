# Table Crm_Line_Discounts

Discount policies for sales documents. Entity: Crm_Line_Discounts

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Discount_Id](#line_discount_id)|`uniqueidentifier` `PK`||
|[Description](#description)|`nvarchar(50)` |The description of the discount that is shown to the operator when he/she should choose between different discounts|
|[From_Date](#from_date)|`datetime` |Starting date of validity of the discount. NULL means no from date restriction|
|[Thru_Date](#thru_date)|`datetime` |Ending date (inclusive) of validity of the discount. If NULL, the discount is valid forever|
|[Target_Group_Id](#target_group_id)|`uniqueidentifier` |Apply the discount only if the customer is included in this target group|
|[Customer_Id](#customer_id)|`uniqueidentifier` |Apply the discount only if this is the customer|
|[Price_List_Id](#price_list_id)|`uniqueidentifier` |Apply the discount only if this price list is used|
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` |Apply the discount only if the product sold is contained in this product group or any of its sub-groups|
|[Product_Id](#product_id)|`uniqueidentifier` |Apply the discount only when this specific product is sold|
|[Min_Quantity](#min_quantity)|`decimal(18, 3)` |Apply the discount only if the quantity sold is equal to or more than the specified here.|
|[Max_Quantity](#max_quantity)|`decimal(18, 3)` |Apply the discount only if the quantity sold is equal to or less than the specified here.|
|[Discount_Percent](#discount_percent)|`decimal(7, 6)` |The discount percent that should be applied if all the matching criteria are met.|
|[Priority](#priority)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`|The priority of this discount policy. When selecting a discount for a sales document line, only the highest priority policy, matching the criteria is applied.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When not NULL, the policy is applied only for documents of the specified enterprise company |
|[Customer_Type_Id](#customer_type_id)|`uniqueidentifier` |Apply the discount only if the customer is of this customer type|
|[Distribution_Channel_Id](#distribution_channel_id)|`uniqueidentifier` |Apply the discount only when the sales document is on the specified channel|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |When set, the policy is applied only for documents of the specified enterprise company location.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_Discount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(50)|

### From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Thru_Date

| Property | Value |
| - | - |
|Type|datetime|

### Target_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Min_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Max_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Priority

| Property | Value |
| - | - |
|Type|tinyint|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Distribution_Channel_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


