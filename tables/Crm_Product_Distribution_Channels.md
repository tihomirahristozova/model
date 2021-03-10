# Table Crm_Product_Distribution_Channels

Channel assignments (listing) for products. Entity: Crm_Product_Distribution_Channels

## Owner Tables Hierarchy

* [Gen_Products](Gen_Products.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Id](#product_id)|`uniqueidentifier` |The listed product|
|[Product_Distribution_Channel_Id](#product_distribution_channel_id)|`uniqueidentifier` `PK`|Product, listed at distribution channel|
|[Distribution_Channel_Id](#distribution_channel_id)|`uniqueidentifier` |The distribution channel in which the product is listed|
|[From_Date](#from_date)|`date` |When the product was listed. NULL-the product was not yet listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does)|
|[To_Date](#to_date)|`date` |When the product was de-listed. NULL=unknown or the product was not de-listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does)|
|[Is_Active](#is_active)|`bit` |Is this product listing active? 1=Yes, 0=No|
|[Minimal_Sales_Price_Per_Lot](#minimal_sales_price_per_lot)|`decimal(18, 4)` |Minimal allowed price for sales of this product through this channel. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. NULL means that there is no minimal sales price enforcement.|
|[Minimal_Sales_Quantity_Base](#minimal_sales_quantity_base)|`decimal(18, 3)` |Minimal base quantity of the current product that has to be specified in any sale for this distribution channel.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Product_Id


Product_Id


The listed product


The listed product

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Product_Distribution_Channels](Crm_Product_Distribution_Channels.md).[Product_Id](Crm_Product_Distribution_Channels.md#product_id)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Product_Distribution_Channel_Id


Product_Distribution_Channel_Id


Product, listed at distribution channel


Product, listed at distribution channel

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
|Derived From|[Crm_Product_Distribution_Channels](Crm_Product_Distribution_Channels.md).[Product_Distribution_Channel_Id](Crm_Product_Distribution_Channels.md#product_distribution_channel_id)|
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

### Distribution_Channel_Id


Distribution_Channel_Id


The distribution channel in which the product is listed


The distribution channel in which the product is listed

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Distribution_Channels](Crm_Distribution_Channels.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Product_Distribution_Channels](Crm_Product_Distribution_Channels.md).[Distribution_Channel_Id](Crm_Product_Distribution_Channels.md#distribution_channel_id)|
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
|Equals|NULL|no|no|

### From_Date


From_Date


When the product was listed. NULL-the product was not yet listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does)


When the product was listed. NULL-the product was not yet listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does)

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
|Default Value|CurrentDate|
|Derived From|[Crm_Product_Distribution_Channels](Crm_Product_Distribution_Channels.md).[From_Date](Crm_Product_Distribution_Channels.md#from_date)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### To_Date


To_Date


When the product was de-listed. NULL=unknown or the product was not de-listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does)


When the product was de-listed. NULL=unknown or the product was not de-listed. The data is for informational purposes only and does not affect the listing status of the product (Is_Active does)

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
|Derived From|[Crm_Product_Distribution_Channels](Crm_Product_Distribution_Channels.md).[To_Date](Crm_Product_Distribution_Channels.md#to_date)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Is_Active


Is_Active


Is this product listing active? 1=Yes, 0=No


Is this product listing active? 1=Yes, 0=No

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
|Derived From|[Crm_Product_Distribution_Channels](Crm_Product_Distribution_Channels.md).[Is_Active](Crm_Product_Distribution_Channels.md#is_active)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Minimal_Sales_Price_Per_Lot


Minimal_Sales_Price_Per_Lot


Minimal allowed price for sales of this product through this channel. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. NULL means that there is no minimal sales price enforcement.


Minimal allowed price for sales of this product through this channel. The price is for one standard lot and in the costing currency of the product. The minimum is enforced upon planning and/or releasing a document. NULL means that there is no minimal sales price enforcement.

| Property | Value |
| - | - |
|Type|decimal(18, 4)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Product_Distribution_Channels](Crm_Product_Distribution_Channels.md).[Minimal_Sales_Price_Per_Lot](Crm_Product_Distribution_Channels.md#minimal_sales_price_per_lot)|
|Format|N2|
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
|Supports EQUALS_IN|no|

### Minimal_Sales_Quantity_Base


Minimal_Sales_Quantity_Base


Minimal base quantity of the current product that has to be specified in any sale for this distribution channel.


Minimal base quantity of the current product that has to be specified in any sale for this distribution channel.

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
|Derived From|[Crm_Product_Distribution_Channels](Crm_Product_Distribution_Channels.md).[Minimal_Sales_Quantity_Base](Crm_Product_Distribution_Channels.md#minimal_sales_quantity_base)|
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
|Derived From|[Crm_Product_Distribution_Channels](Crm_Product_Distribution_Channels.md).[Row_Version](Crm_Product_Distribution_Channels.md#row_version)|
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


