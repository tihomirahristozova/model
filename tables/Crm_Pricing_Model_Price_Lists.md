# Table Crm_Pricing_Model_Price_Lists

The price lists, which are updated by the pricing model. Entity: Crm_Pricing_Model_Price_Lists

## Owner Tables Hierarchy

* [Crm_Pricing_Models](Crm_Pricing_Models.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Pricing_Model_Price_List_Id](#pricing_model_price_list_id)|`uniqueidentifier` `PK`|Pricing Model Price List|
|[Pricing_Model_Id](#pricing_model_id)|`uniqueidentifier` |The pricing model, for which the price list is listed|
|[Line_No](#line_no)|`int` |The consecutive number of this price list within the pricing model|
|[Price_List_Id](#price_list_id)|`uniqueidentifier` |The price list, which is included in the pricing model|
|[Margin_Percent](#margin_percent)|`decimal(6, 5)` |Used, when the price will be automatically calculated as percentage difference from standard price. It is usually a negative value. NULL, when the price will not be automatically calculated in this way|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Pricing_Model_Price_List_Id


Pricing_Model_Price_List_Id


Pricing Model Price List


Pricing Model Price List

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
|Derived From|[Crm_Pricing_Model_Price_Lists](Crm_Pricing_Model_Price_Lists.md).[Pricing_Model_Price_List_Id](Crm_Pricing_Model_Price_Lists.md#pricing_model_price_list_id)|
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

### Pricing_Model_Id


Pricing_Model_Id


The pricing model, for which the price list is listed


The pricing model, for which the price list is listed

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Crm_Pricing_Models](Crm_Pricing_Models.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Pricing_Model_Price_Lists](Crm_Pricing_Model_Price_Lists.md).[Pricing_Model_Id](Crm_Pricing_Model_Price_Lists.md#pricing_model_id)|
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

### Line_No


Line_No


The consecutive number of this price list within the pricing model


The consecutive number of this price list within the pricing model

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|1|
|Derived From|[Crm_Pricing_Model_Price_Lists](Crm_Pricing_Model_Price_Lists.md).[Line_No](Crm_Pricing_Model_Price_Lists.md#line_no)|
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

### Price_List_Id


Price_List_Id


The price list, which is included in the pricing model


The price list, which is included in the pricing model

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Price_Lists](Crm_Price_Lists.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Pricing_Model_Price_Lists](Crm_Pricing_Model_Price_Lists.md).[Price_List_Id](Crm_Pricing_Model_Price_Lists.md#price_list_id)|
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

### Margin_Percent


Margin_Percent


Used, when the price will be automatically calculated as percentage difference from standard price. It is usually a negative value. NULL, when the price will not be automatically calculated in this way


Used, when the price will be automatically calculated as percentage difference from standard price. It is usually a negative value. NULL, when the price will not be automatically calculated in this way

| Property | Value |
| - | - |
|Type|decimal(6, 5)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsPercent|
|Default Value|None|
|Derived From|[Crm_Pricing_Model_Price_Lists](Crm_Pricing_Model_Price_Lists.md).[Margin_Percent](Crm_Pricing_Model_Price_Lists.md#margin_percent)|
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
|Derived From|[Crm_Pricing_Model_Price_Lists](Crm_Pricing_Model_Price_Lists.md).[Row_Version](Crm_Pricing_Model_Price_Lists.md#row_version)|
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


