# Table Cms_Product_Catalog_Web_Modules

A web module, which presents a whole product catalog. Entity: Cms_Product_Catalog_Web_Modules

## Owner Tables Hierarchy

* [Cms_Web_Modules](Cms_Web_Modules.md)
* [Cms_Web_Sites](Cms_Web_Sites.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Catalog_Web_Module_Id](#product_catalog_web_module_id)|`uniqueidentifier` `PK`||
|[Web_Module_Id](#web_module_id)|`uniqueidentifier` |The base web module, which this module inherits.|
|[Product_Catalog_Id](#product_catalog_id)|`uniqueidentifier` |The product catalog, which is represented by this web module.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Product_Catalog_Web_Module_Id


Product_Catalog_Web_Module_Id

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
|Derived From|[Cms_Product_Catalog_Web_Modules](Cms_Product_Catalog_Web_Modules.md).[Product_Catalog_Web_Module_Id](Cms_Product_Catalog_Web_Modules.md#product_catalog_web_module_id)|
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

### Web_Module_Id


Web_Module_Id


The base web module, which this module inherits.


The base web module, which this module inherits.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Cms_Web_Modules](Cms_Web_Modules.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cms_Product_Catalog_Web_Modules](Cms_Product_Catalog_Web_Modules.md).[Web_Module_Id](Cms_Product_Catalog_Web_Modules.md#web_module_id)|
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

### Product_Catalog_Id


Product_Catalog_Id


The product catalog, which is represented by this web module.


The product catalog, which is represented by this web module.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Product_Catalogs](Gen_Product_Catalogs.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cms_Product_Catalog_Web_Modules](Cms_Product_Catalog_Web_Modules.md).[Product_Catalog_Id](Cms_Product_Catalog_Web_Modules.md#product_catalog_id)|
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
|Derived From|[Cms_Product_Catalog_Web_Modules](Cms_Product_Catalog_Web_Modules.md).[Row_Version](Cms_Product_Catalog_Web_Modules.md#row_version)|
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


