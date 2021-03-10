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


Product_Catalog_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Product_Catalog_Id](Gen_Product_Catalogs.md#product_catalog_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Product_Catalog_Code


Product_Catalog_Code


Unique catalog code.


Unique catalog code.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Product_Catalog_Code](Gen_Product_Catalogs.md#product_catalog_code)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Product_Catalog_Name


Product_Catalog_Name


Product catalog name (multilanguage).


Product catalog name (multilanguage).

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Product_Catalog_Name](Gen_Product_Catalogs.md#product_catalog_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Root_Product_Group_Id


Root_Product_Group_Id


The root (starting) product group of the catalog. Each catalog starts from a root product group and includes the products in the sub-groups.


The root (starting) product group of the catalog. Each catalog starts from a root product group and includes the products in the sub-groups.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Product_Groups](Gen_Product_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Root_Product_Group_Id](Gen_Product_Catalogs.md#root_product_group_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Notes](Gen_Product_Catalogs.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Logo


Logo


The logo of the product catalog. Used for web and other visualization of the catalog.


The logo of the product catalog. Used for web and other visualization of the catalog.

| Property | Value |
| - | - |
|Type|varbinary|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Logo](Gen_Product_Catalogs.md#logo)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|yes|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Header_Html


Header_Html


The header of the catalog in HTML format. Primarily used for web visualizations of the catalog. NULL specifies that there shouldn't be any user-defined header.


The header of the catalog in HTML format. Primarily used for web visualizations of the catalog. NULL specifies that there shouldn't be any user-defined header.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Header_Html](Gen_Product_Catalogs.md#header_html)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Footer_Html


Footer_Html


The footer of the catalog in HTML format. Primarily used for web visualizations of the catalog. NULL means that there shouldn't be any user-defined footer.


The footer of the catalog in HTML format. Primarily used for web visualizations of the catalog. NULL means that there shouldn't be any user-defined footer.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Footer_Html](Gen_Product_Catalogs.md#footer_html)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Background_Image


Background_Image


The background image to be used for web visualization of the catalog. NULL means that background image won't be displayed.


The background image to be used for web visualization of the catalog. NULL means that background image won't be displayed.

| Property | Value |
| - | - |
|Type|varbinary|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Background_Image](Gen_Product_Catalogs.md#background_image)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|yes|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Background_Position_Horizontal


Background_Position_Horizontal


Horizontal position of the Background Image. L=Left, C=Center, R=Right.


Horizontal position of the Background Image. L=Left, C=Center, R=Right.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`L`, `C`, `R`|
|Default Value|L|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Background_Position_Horizontal](Gen_Product_Catalogs.md#background_position_horizontal)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Background_Position_Vertical


Background_Position_Vertical


Vertical position of the Background Image. T=Top, C=Center, B=Bottom.


Vertical position of the Background Image. T=Top, C=Center, B=Bottom.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`T`, `C`, `B`|
|Default Value|T|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Background_Position_Vertical](Gen_Product_Catalogs.md#background_position_vertical)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Background_Repeat


Background_Repeat


Specifies if and how the background image will be repeated. R=Repeat both vertically and horizontally; X=Repeat only horizontally; Y=Repeat only vertically; N=No repeat.


Specifies if and how the background image will be repeated. R=Repeat both vertically and horizontally; X=Repeat only horizontally; Y=Repeat only vertically; N=No repeat.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`R`, `X`, `Y`, `N`|
|Default Value|R|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Background_Repeat](Gen_Product_Catalogs.md#background_repeat)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Background_Color


Background_Color


When not NULL, specifies the background color to use for visualization of the catalog. The color is in RGBA color format.


When not NULL, specifies the background color to use for visualization of the catalog. The color is in RGBA color format.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Background_Color](Gen_Product_Catalogs.md#background_color)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Row_Version](Gen_Product_Catalogs.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Web_Site_Id


Web_Site_Id


The ECommerce web site, which will be used to host the product catalog. When NULL, the product catalog would not be hosted with internal ECommerce site.


The ECommerce web site, which will be used to host the product catalog. When NULL, the product catalog would not be hosted with internal ECommerce site.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sys_Web_Sites](Sys_Web_Sites.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Catalogs](Gen_Product_Catalogs.md).[Web_Site_Id](Gen_Product_Catalogs.md#web_site_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|14|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Root_Product_Group_Id_L1_Name


Root_Product_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Root_Product_Group_Id_L2_Name


Root_Product_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Root_Product_Group_Id_L3_Name


Root_Product_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Root_Product_Group_Id_L4_Name


Root_Product_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Root_Product_Group_Id_L5_Name


Root_Product_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Root_Product_Group_Id_L6_Name


Root_Product_Group_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


