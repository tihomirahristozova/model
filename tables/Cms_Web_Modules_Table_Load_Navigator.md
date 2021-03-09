# Query Cms_Web_Modules_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Web_Module_Id](#web_module_id)|`uniqueidentifier` `PK`||
|[Web_Site_Id](#web_site_id)|`uniqueidentifier` |The web site to which the module belongs.|
|[Parent_Web_Module_Id](#parent_web_module_id)|`uniqueidentifier` |The parent web Module. It can only be a module with Module Type = Category. Null means that the web Module is root web Module.|
|[Web_Module_Name](#web_module_name)|`nvarchar` |Multilanguage Module name. This is used as a title when displaying the web Module.|
|[Local_Url](#local_url)|`nvarchar` |The local Module Url. The full Url of a module is formed based on the sites Base Url, the local Urls of all parent modules and the module Local Url. Null means that the web Module is the default web module within the parent path.|
|[Is_Published](#is_published)|`bit` |Specifies whether the module is published and will be showed in the web site.|
|[Module_Picture](#module_picture)|`varbinary` |Default picture. Used for picture links, small module icons, etc. PNG format is suggested.|
|[Module_Type](#module_type)|`nvarchar` Allowed: `CAT`, `STA`, `NEW`|Specifies the content handler. The content handler is responsible for generating the actual web page content. Module Types include Category, Static, News, Product, etc.|

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
|Type|nvarchar|

### Local_Url

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|


