# Table Crm_Bonus_Programs

Bonus programs allow automatic adding of new line with bonus product or automatic application of discount in a sales document. Entity: Crm_Bonus_Programs

## Summary

| Name | Type | Description |
| - | - | --- |
|[Bonus_Program_Id](#bonus_program_id)|`uniqueidentifier` `PK`||
|[Bonus_Program_Name](#bonus_program_name)|`nvarchar(254)` `ML`|The name of the bonus program|
|[Condition_Product_Id](#condition_product_id)|`uniqueidentifier` |When not NULL, specifies a conditional product, which is required to exist in the sales document in order for the bonus program to be applied. If a condition with multiple products is required, additional products can be added to Bonus Program Products. If NULL the other conditions should be evaluated against the whole order.|
|[Condition_Min_Quantity](#condition_min_quantity)|`decimal(12, 3)` |When not NULL, specifies condition for the bonus - minimal quantity of the condition product. If the condition product is null, this cannot be specified|
|[Condition_Max_Quantity](#condition_max_quantity)|`decimal(12, 3)` |When not NULL, specifies condition for the bonus - maximal quantity of the condition product. If the condition product is null, this cannot be specified|
|[Condition_Min_Amount](#condition_min_amount)|`decimal(12, 2)` |If not NULL specifies the minimal amount for which the bonus is valid. NULL means that there is no minimal amount condition for the bonus|
|[Condition_Max_Amount](#condition_max_amount)|`decimal(12, 2)` |If not NULL specifies the maximal amount for which the bonus is valid. NULL means that there is no maximal amount condition for the bonus|
|[Condition_Document_Currency_Id](#condition_document_currency_id)|`uniqueidentifier` |Condition for the document amount. Should be not NULL if any of the amount conditions are not NULL|
|[Condition_From_Date](#condition_from_date)|`datetime` |Starting date of the bonus. NULL means that there is no starting date restriction|
|[Condition_To_Date](#condition_to_date)|`datetime` |Ending date (inclusive) of the bonus. NULL means that there is no ending date restriction|
|[Condition_Target_Group_Id](#condition_target_group_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only to the specified target customer group|
|[Condition_Customer_Id](#condition_customer_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only to the specified customer|
|[Condition_Customer_Filter_XML](#condition_customer_filter_xml)|`nvarchar(2147483647)` |When not NULL, specifies that the bonus should be applied only to customers who meet the specified criteria. The criteria could include custom properties|
|[Condition_Ship_To_Customer_Id](#condition_ship_to_customer_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only when shipping to the specified customer|
|[Condition_Ship_To_Customer_Filter_XML](#condition_ship_to_customer_filter_xml)|`nvarchar(2147483647)` |When not NULL, specifies that the bonus should be applied only when shipping to customer with the specified characteristics|
|[Condition_Price_List_Id](#condition_price_list_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only when the sales order is based on the speicfied price list|
|[Active](#active)|`bit` |General condition if the bonus is active. The other conditions are verified only for active bonus programs|
|[Bonus_Action](#bonus_action)|`nvarchar(1)` Allowed: `P`, `D`|Bonus action: P-Add product to the order, A-Add amount, D-Give discount|
|[Bonus_Product_Id](#bonus_product_id)|`uniqueidentifier` |The product that is rewarded if the bonus conditions are met. NULL means that the bonus reward is not product|
|[Bonus_Product_Quantity](#bonus_product_quantity)|`decimal(12, 3)` |The quantity rewarded of the bonus product. Should be not NULL if and only when the bonus product is not NULL|
|[Bonus_Product_Quantity_Unit_Id](#bonus_product_quantity_unit_id)|`uniqueidentifier` |The measurement unit of the quantity rewarded of the bonus product. Should be not NULL if and only when the bonus product is not NULL|
|[Bonus_Product_Quantity_Multiplier_For_Each_Lot_Size](#bonus_product_quantity_multiplier_for_each_lot_size)|`decimal(12, 3)` |When not NULL, specifies that the bonus quantity should be multiplied for each of the specified lot size. Can be non-NULL only when condition product is specified|
|[Bonus_Document_Amount_Type_Id](#bonus_document_amount_type_id)|`uniqueidentifier` |When not NULL specifies that a document amount should be added to the order when the bonus conditions are met. NULL means that the bonus reward is not a document amount|
|[Bonus_Document_Amount_Percent](#bonus_document_amount_percent)|`decimal(7, 6)` |The percent of the document amount that is rewarded. Should be NULL if and only if the bonus document amount is NULL|
|[Bonus_Line_Discount_Percent](#bonus_line_discount_percent)|`decimal(7, 6)` |The percent discount to be applied to bonus lines. Used only for bonus programs with Action = D (Discount)|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When set, specifies that the sales document must be of the specified enterprise company.|
|[Priority](#priority)|`tinyint` Allowed: `0`, `1`, `2`, `3`, `4`|Priority (1-5) of the bonus program comparative to the other bonus programs. 1 is the lowest priority|
|[Condition_Distribution_Channel_Id](#condition_distribution_channel_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only when the specified channel is used|
|[Condition_Distribution_Channel_Filter_XML](#condition_distribution_channel_filter_xml)|`nvarchar(2147483647)` |When not NULL, specifies that the bonus should be applied only when the distribution channel of the sales order has the specified characteristics|
|[Condition_Product_Group_Id](#condition_product_group_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only to products from the specified product group or its subgroups|
|[Row_Version](#row_version)|`timestamp` ||
|[Company_Location_Id](#company_location_id)|`uniqueidentifier` |When set, specifies that the sales document must be of the specified enterprise company location.|

## Columns

### Bonus_Program_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bonus_Program_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Condition_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Min_Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Condition_Max_Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Condition_Min_Amount

| Property | Value |
| - | - |
|Type|decimal(12, 2)|

### Condition_Max_Amount

| Property | Value |
| - | - |
|Type|decimal(12, 2)|

### Condition_Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Condition_To_Date

| Property | Value |
| - | - |
|Type|datetime|

### Condition_Target_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Customer_Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Condition_Ship_To_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Ship_To_Customer_Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Condition_Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Bonus_Action

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Bonus_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bonus_Product_Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Bonus_Product_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bonus_Product_Quantity_Multiplier_For_Each_Lot_Size

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Bonus_Document_Amount_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bonus_Document_Amount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Bonus_Line_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Priority

| Property | Value |
| - | - |
|Type|tinyint|

### Condition_Distribution_Channel_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Distribution_Channel_Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Condition_Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


