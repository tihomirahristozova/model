# Table Cms_Web_Modules

The abstract basic building block of web sites. Each module can render multiple web pages. Entity: Cms_Web_Modules

## Owner Tables Hierarchy

* [Cms_Web_Sites](Cms_Web_Sites.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Web_Module_Id](#web_module_id)|`uniqueidentifier` `PK`||
|[Web_Site_Id](#web_site_id)|`uniqueidentifier` |The web site to which the module belongs.|
|[Parent_Web_Module_Id](#parent_web_module_id)|`uniqueidentifier` |The parent web Module. It can only be a module with Module Type = Category. Null means that the web Module is root web Module.|
|[Web_Module_Name](#web_module_name)|`nvarchar(512)` |Multilanguage Module name. This is used as a title when displaying the web Module.|
|[Local_Url](#local_url)|`nvarchar(128)` |The local Module Url. The full Url of a module is formed based on the sites Base Url, the local Urls of all parent modules and the module Local Url. Null means that the web Module is the default web module within the parent path.|
|[Is_Published](#is_published)|`bit` |Specifies whether the module is published and will be showed in the web site.|
|[Module_Picture](#module_picture)|`varbinary` |Default picture. Used for picture links, small module icons, etc. PNG format is suggested.|
|[Module_Type](#module_type)|`nvarchar(3)` Allowed: `CAT`, `STA`, `NEW`|Specifies the content handler. The content handler is responsible for generating the actual web page content. Module Types include Category, Static, News, Product, etc.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Web_Module_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Web_Site_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Web_Module_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Web_Module_Name

| Property | Value |
| - | - |
|Type|nvarchar(512)|

### Local_Url

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Is_Published

| Property | Value |
| - | - |
|Type|bit|

### Module_Picture

| Property | Value |
| - | - |
|Type|varbinary|

### Module_Type

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


