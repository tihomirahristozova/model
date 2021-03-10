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


Promotional_Package_Code


Unique code of the promotional package


Unique code of the promotional package

| Property | Value |
| - | - |
|Type|nvarchar(20)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Promotional_Package_Code](Crm_Promotional_Packages.md#promotional_package_code)|
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
|Max Length|20|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Promotional_Package_Name


Promotional_Package_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Promotional_Package_Name](Crm_Promotional_Packages.md#promotional_package_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Active


Active


Package status: 1 = the offer is available for new documents; 0 = otherwise


Package status: 1 = the offer is available for new documents; 0 = otherwise

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Active](Crm_Promotional_Packages.md#active)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Valid_From_Date


Valid_From_Date


When not NULL specifies the first date when the package is valid for offering. The date is compared against the document date


When not NULL specifies the first date when the package is valid for offering. The date is compared against the document date

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Valid_From_Date](Crm_Promotional_Packages.md#valid_from_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Valid_To_Date


Valid_To_Date


When not NULL specifies the last date (inclusive) when the package is valid. The date is compared against the document date


When not NULL specifies the last date (inclusive) when the package is valid. The date is compared against the document date

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Valid_To_Date](Crm_Promotional_Packages.md#valid_to_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Valid_For_Price_List_Id


Valid_For_Price_List_Id


When not NULL, the package is valid only for the specified price list


When not NULL, the package is valid only for the specified price list

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Price_Lists](Crm_Price_Lists.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Valid_For_Price_List_Id](Crm_Promotional_Packages.md#valid_for_price_list_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Valid_For_Customer_Id


Valid_For_Customer_Id


When not NULL, the package is valid only for the specified customer


When not NULL, the package is valid only for the specified customer

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Customers](Crm_Customers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Valid_For_Customer_Id](Crm_Promotional_Packages.md#valid_for_customer_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Valid_For_Target_Group_Id


Valid_For_Target_Group_Id


When not NULL, the package is valid only for the specified customer target group


When not NULL, the package is valid only for the specified customer target group

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Target_Groups](Crm_Target_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Valid_For_Target_Group_Id](Crm_Promotional_Packages.md#valid_for_target_group_id)|
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
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Valid_For_Customer_Filter_XML


Valid_For_Customer_Filter_XML


When not NULL, the package is valid only for the customers, that match the filter


When not NULL, the package is valid only for the customers, that match the filter

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Valid_For_Customer_Filter_XML](Crm_Promotional_Packages.md#valid_for_customer_filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Valid_For_Distribution_Channel_Filter_XML


Valid_For_Distribution_Channel_Filter_XML


When not NULL, the package is valid only if the specified distribution channel of the sales order fits in the filter criteria.


When not NULL, the package is valid only if the specified distribution channel of the sales order fits in the filter criteria.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Valid_For_Distribution_Channel_Filter_XML](Crm_Promotional_Packages.md#valid_for_distribution_channel_filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Valid_For_Distribution_Channel_Id


Valid_For_Distribution_Channel_Id


When not NULL, the package is valid only for the specified distribution channel of the sales order


When not NULL, the package is valid only for the specified distribution channel of the sales order

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Distribution_Channels](Crm_Distribution_Channels.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Valid_For_Distribution_Channel_Id](Crm_Promotional_Packages.md#valid_for_distribution_channel_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Enterprise_Company_Id


Enterprise_Company_Id


When not NULL, indicates that the package is valid only for the specified enterprise company.


When not NULL, indicates that the package is valid only for the specified enterprise company.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Enterprise_Company_Id](Crm_Promotional_Packages.md#enterprise_company_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Promotional_Package_Id


Promotional_Package_Id

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
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Promotional_Package_Id](Crm_Promotional_Packages.md#promotional_package_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Valid_For_Ship_To_Customer_Id


Valid_For_Ship_To_Customer_Id


When not NULL, specifies that the package is valid only when the sales document is for the specified Ship To Customer.


When not NULL, specifies that the package is valid only when the sales document is for the specified Ship To Customer.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Customers](Crm_Customers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Valid_For_Ship_To_Customer_Id](Crm_Promotional_Packages.md#valid_for_ship_to_customer_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

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
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Row_Version](Crm_Promotional_Packages.md#row_version)|
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

### Valid_For_Ship_To_Customer_Filter_XML


Valid_For_Ship_To_Customer_Filter_XML


When not NULL, specifies validity condition for the Ship To Customer of the sales document.


When not NULL, specifies validity condition for the Ship To Customer of the sales document.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Valid_For_Ship_To_Customer_Filter_XML](Crm_Promotional_Packages.md#valid_for_ship_to_customer_filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Enterprise_Company_Location_Id


Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Company_Locations](Cm_Company_Locations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Promotional_Packages](Crm_Promotional_Packages.md).[Enterprise_Company_Location_Id](Crm_Promotional_Packages.md#enterprise_company_location_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|


