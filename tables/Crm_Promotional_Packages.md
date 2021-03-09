# Table Crm_Promotional_Packages

Promotional packages are packages of products, which are sold together at a special pricing and discount conditions. Entity: Crm_Promotional_Packages

## Summary

| Name | Type | Description |
| - | - | --- |
|[Promotional_Package_Code](#promotional_package_code)|`nvarchar(20)` |Unique code of the promotional package|
|[Promotional_Package_Name](#promotional_package_name)|`nvarchar(254)` ||
|[Active](#active)|`bit` |Package status: 1 = the offer is available for new documents; 0 = otherwise|
|[Valid_From_Date](#valid_from_date)|`date` |When not NULL specifies the first date when the package is valid for offering. The date is compared against the document date|
|[Valid_To_Date](#valid_to_date)|`date` |When not NULL specifies the last date (inclusive) when the package is valid. The date is compared against the document date|
|[Valid_For_Price_List_Id](#valid_for_price_list_id)|`uniqueidentifier` |When not NULL, the package is valid only for the specified price list|
|[Valid_For_Customer_Id](#valid_for_customer_id)|`uniqueidentifier` |When not NULL, the package is valid only for the specified customer|
|[Valid_For_Target_Group_Id](#valid_for_target_group_id)|`uniqueidentifier` |When not NULL, the package is valid only for the specified customer target group|
|[Valid_For_Customer_Filter_XML](#valid_for_customer_filter_xml)|`nvarchar(2147483647)` |When not NULL, the package is valid only for the customers, that match the filter|
|[Valid_For_Distribution_Channel_Filter_XML](#valid_for_distribution_channel_filter_xml)|`nvarchar(2147483647)` |When not NULL, the package is valid only if the specified distribution channel of the sales order fits in the filter criteria.|
|[Valid_For_Distribution_Channel_Id](#valid_for_distribution_channel_id)|`uniqueidentifier` |When not NULL, the package is valid only for the specified distribution channel of the sales order|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When not NULL, indicates that the package is valid only for the specified enterprise company.|
|[Promotional_Package_Id](#promotional_package_id)|`uniqueidentifier` `PK`||
|[Valid_For_Ship_To_Customer_Id](#valid_for_ship_to_customer_id)|`uniqueidentifier` |When not NULL, specifies that the package is valid only when the sales document is for the specified Ship To Customer.|
|[Row_Version](#row_version)|`timestamp` ||
|[Valid_For_Ship_To_Customer_Filter_XML](#valid_for_ship_to_customer_filter_xml)|`nvarchar(2147483647)` |When not NULL, specifies validity condition for the Ship To Customer of the sales document.|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||

## Columns

### Promotional_Package_Code

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Promotional_Package_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Valid_From_Date

| Property | Value |
| - | - |
|Type|date|

### Valid_To_Date

| Property | Value |
| - | - |
|Type|date|

### Valid_For_Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valid_For_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valid_For_Target_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valid_For_Customer_Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Valid_For_Distribution_Channel_Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Valid_For_Distribution_Channel_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Promotional_Package_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valid_For_Ship_To_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Valid_For_Ship_To_Customer_Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


