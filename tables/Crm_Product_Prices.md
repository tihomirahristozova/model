# Table Crm_Product_Prices

Specific prices of products. A price is applied after matching the specified criteria. Entity: Crm_Product_Prices

## Summary

| Name | Type | Description |
| - | - | --- |
|[Price_List_Id](#price_list_id)|`uniqueidentifier` |When not NULL, specifies that the sales document must have the specified price list.|
|[Price](#price)|`decimal(13, 5)` |Price in the specified currency and for the specified quantity|
|[Currency_Id](#currency_id)|`uniqueidentifier` |The currency of the price|
|[Price_Quantity_Measurement_Unit_Id](#price_quantity_measurement_unit_id)|`uniqueidentifier` |The measurement unit of Price_Quantity|
|[Customer_Id](#customer_id)|`uniqueidentifier` |When not NULL, specifies that the customer of the sales document must be the specified customer.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When not NULL, specifies that the sales document must be in the specified enterprise company.|
|[Priority](#priority)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the price comparative to other prices. Only the highest priority price is applied.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Min_Quantity](#min_quantity)|`decimal(18, 3)` |Minimal quantity required to use this price (in the Price_Quantity_Measurement_Unit)|
|[Max_Quantity](#max_quantity)|`decimal(18, 3)` |Maximum quantity for which this price is valid in the Price_Quantity_Measurement_Unit|
|[From_Date](#from_date)|`date` |Starting date of validity of the price|
|[Thru_Date](#thru_date)|`date` |Ending date (inclusive) of the validity of the price|
|[Target_Group_Id](#target_group_id)|`uniqueidentifier` |When not NULL, specifies a criteria, which is matched only when the customer of the sales document is included in the group.|
|[Price_Type_Id](#price_type_id)|`uniqueidentifier` |Price type of the current product price. The price types are used to set additional priority condition for the prices.|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |When set, specifies that the sales document must be of the specified enterprise company location.|
|[Distribution_Channel_Id](#distribution_channel_id)|`uniqueidentifier` |Use the price only when selling through the specified channel|
|[Product_Price_Id](#product_price_id)|`uniqueidentifier` `PK`||
|[Price_Quantity](#price_quantity)|`decimal(10, 3)` |The quantity of the product for which the price is specified|
|[Product_Id](#product_id)|`uniqueidentifier` |The product for which a price will be defined|
|[Ship_To_Customer_Id](#ship_to_customer_id)|`uniqueidentifier` |When not null, specifies that the price will be applied only when the sales document has the specified Ship-To-Customer.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Price_List_Id


Price_List_Id


When not NULL, specifies that the sales document must have the specified price list.


When not NULL, specifies that the sales document must have the specified price list.

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
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Price_List_Id](Crm_Product_Prices.md#price_list_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Price


Price


Price in the specified currency and for the specified quantity


Price in the specified currency and for the specified quantity

| Property | Value |
| - | - |
|Type|decimal(13, 5)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Price](Crm_Product_Prices.md#price)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|GreaterThanOrLessThan|None|yes|no|

### Currency_Id


Currency_Id


The currency of the price


The currency of the price

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Currencies](Gen_Currencies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Currency_Id](Crm_Product_Prices.md#currency_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Price_Quantity_Measurement_Unit_Id


Price_Quantity_Measurement_Unit_Id


The measurement unit of Price_Quantity


The measurement unit of Price_Quantity

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Price_Quantity_Measurement_Unit_Id](Crm_Product_Prices.md#price_quantity_measurement_unit_id)|
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
|UI Width|Short|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Customer_Id


Customer_Id


When not NULL, specifies that the customer of the sales document must be the specified customer.


When not NULL, specifies that the customer of the sales document must be the specified customer.

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
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Customer_Id](Crm_Product_Prices.md#customer_id)|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Enterprise_Company_Id


Enterprise_Company_Id


When not NULL, specifies that the sales document must be in the specified enterprise company.


When not NULL, specifies that the sales document must be in the specified enterprise company.

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
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Enterprise_Company_Id](Crm_Product_Prices.md#enterprise_company_id)|
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
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Priority


Priority


Priority of the price comparative to other prices. Only the highest priority price is applied.


Priority of the price comparative to other prices. Only the highest priority price is applied.

| Property | Value |
| - | - |
|Type|tinyint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`1`, `2`, `3`, `4`, `5`|
|Default Value|2|
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Priority](Crm_Product_Prices.md#priority)|
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
|UI Width|Short|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Notes](Crm_Product_Prices.md#notes)|
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
|Visible|no|
|Max Length|254|
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Min_Quantity


Min_Quantity


Minimal quantity required to use this price (in the Price_Quantity_Measurement_Unit)


Minimal quantity required to use this price (in the Price_Quantity_Measurement_Unit)

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Min_Quantity](Crm_Product_Prices.md#min_quantity)|
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
|Visible|no|
|Max Length|-1|
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Max_Quantity


Max_Quantity


Maximum quantity for which this price is valid in the Price_Quantity_Measurement_Unit


Maximum quantity for which this price is valid in the Price_Quantity_Measurement_Unit

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Max_Quantity](Crm_Product_Prices.md#max_quantity)|
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
|Visible|no|
|Max Length|-1|
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### From_Date


From_Date


Starting date of validity of the price


Starting date of validity of the price

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
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[From_Date](Crm_Product_Prices.md#from_date)|
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
|Visible|no|
|Max Length|-1|
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Thru_Date


Thru_Date


Ending date (inclusive) of the validity of the price


Ending date (inclusive) of the validity of the price

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
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Thru_Date](Crm_Product_Prices.md#thru_date)|
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
|Visible|no|
|Max Length|-1|
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Target_Group_Id


Target_Group_Id


When not NULL, specifies a criteria, which is matched only when the customer of the sales document is included in the group.


When not NULL, specifies a criteria, which is matched only when the customer of the sales document is included in the group.

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
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Target_Group_Id](Crm_Product_Prices.md#target_group_id)|
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
|Visible|no|
|Max Length|-1|
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Price_Type_Id


Price_Type_Id


Price type of the current product price. The price types are used to set additional priority condition for the prices.


Price type of the current product price. The price types are used to set additional priority condition for the prices.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Price_Types](Crm_Price_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Price_Type_Id](Crm_Product_Prices.md#price_type_id)|
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

### Enterprise_Company_Location_Id


Enterprise_Company_Location_Id


When set, specifies that the sales document must be of the specified enterprise company location.


When set, specifies that the sales document must be of the specified enterprise company location.

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
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Enterprise_Company_Location_Id](Crm_Product_Prices.md#enterprise_company_location_id)|
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

### Distribution_Channel_Id


Distribution_Channel_Id


Use the price only when selling through the specified channel


Use the price only when selling through the specified channel

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
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Distribution_Channel_Id](Crm_Product_Prices.md#distribution_channel_id)|
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

### Product_Price_Id


Product_Price_Id

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
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Product_Price_Id](Crm_Product_Prices.md#product_price_id)|
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
|Equals|NULL|no|no|

### Price_Quantity


Price_Quantity


The quantity of the product for which the price is specified


The quantity of the product for which the price is specified

| Property | Value |
| - | - |
|Type|decimal(10, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Price_Quantity](Crm_Product_Prices.md#price_quantity)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Product_Id


Product_Id


The product for which a price will be defined


The product for which a price will be defined

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Product_Id](Crm_Product_Prices.md#product_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Ship_To_Customer_Id


Ship_To_Customer_Id


When not null, specifies that the price will be applied only when the sales document has the specified Ship-To-Customer.


When not null, specifies that the price will be applied only when the sales document has the specified Ship-To-Customer.

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
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Ship_To_Customer_Id](Crm_Product_Prices.md#ship_to_customer_id)|
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
|Derived From|[Crm_Product_Prices](Crm_Product_Prices.md).[Row_Version](Crm_Product_Prices.md#row_version)|
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


