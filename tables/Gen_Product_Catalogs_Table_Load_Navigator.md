# Query Gen_Product_Catalogs_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Catalog_Id](#product_catalog_id)|`uniqueidentifier` `PK`||
|[Product_Catalog_Code](#product_catalog_code)|`nvarchar` |Unique catalog code.|
|[Product_Catalog_Name](#product_catalog_name)|`nvarchar` `ML`|Product catalog name (multilanguage).|
|[Root_Product_Group_Id](#root_product_group_id)|`uniqueidentifier` |The root (starting) product group of the catalog. Each catalog starts from a root product group and includes the products in the sub-groups.|
|[Notes](#notes)|`nvarchar` ||
|[Logo](#logo)|`varbinary` |The logo of the product catalog. Used for web and other visualization of the catalog.|
|[Header_Html](#header_html)|`nvarchar` |The header of the catalog in HTML format. Primarily used for web visualizations of the catalog. NULL specifies that there shouldn't be any user-defined header.|
|[Footer_Html](#footer_html)|`nvarchar` |The footer of the catalog in HTML format. Primarily used for web visualizations of the catalog. NULL means that there shouldn't be any user-defined footer.|
|[Background_Image](#background_image)|`varbinary` |The background image to be used for web visualization of the catalog. NULL means that background image won't be displayed.|
|[Background_Position_Horizontal](#background_position_horizontal)|`nvarchar` Allowed: `L`, `C`, `R`|Horizontal position of the Background Image. L=Left, C=Center, R=Right.|
|[Background_Position_Vertical](#background_position_vertical)|`nvarchar` Allowed: `T`, `C`, `B`|Vertical position of the Background Image. T=Top, C=Center, B=Bottom.|
|[Background_Repeat](#background_repeat)|`nvarchar` Allowed: `R`, `X`, `Y`, `N`|Specifies if and how the background image will be repeated. R=Repeat both vertically and horizontally; X=Repeat only horizontally; Y=Repeat only vertically; N=No repeat.|
|[Background_Color](#background_color)|`int` |When not NULL, specifies the background color to use for visualization of the catalog. The color is in RGBA color format.|
|[Row_Version](#row_version)|`timestamp` ||
|[Web_Site_Id](#web_site_id)|`uniqueidentifier` |The ECommerce web site, which will be used to host the product catalog. When NULL, the product catalog would not be hosted with internal ECommerce site.|
|[Root_Product_Group_Id_L1_Name](#root_product_group_id_l1_name)|`nvarchar` `ML`||
|[Root_Product_Group_Id_L2_Name](#root_product_group_id_l2_name)|`nvarchar` `ML`||
|[Root_Product_Group_Id_L3_Name](#root_product_group_id_l3_name)|`nvarchar` `ML`||
|[Root_Product_Group_Id_L4_Name](#root_product_group_id_l4_name)|`nvarchar` `ML`||
|[Root_Product_Group_Id_L5_Name](#root_product_group_id_l5_name)|`nvarchar` `ML`||
|[Root_Product_Group_Id_L6_Name](#root_product_group_id_l6_name)|`nvarchar` `ML`||

## Columns

### Product_Catalog_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Catalog_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Catalog_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Root_Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Logo

| Property | Value |
| - | - |
|Type|varbinary|

### Header_Html

| Property | Value |
| - | - |
|Type|nvarchar|

### Footer_Html

| Property | Value |
| - | - |
|Type|nvarchar|

### Background_Image

| Property | Value |
| - | - |
|Type|varbinary|

### Background_Position_Horizontal

| Property | Value |
| - | - |
|Type|nvarchar|

### Background_Position_Vertical

| Property | Value |
| - | - |
|Type|nvarchar|

### Background_Repeat

| Property | Value |
| - | - |
|Type|nvarchar|

### Background_Color

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Web_Site_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Root_Product_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Root_Product_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Root_Product_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Root_Product_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Root_Product_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Root_Product_Group_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


