# Table Cms_Static_Web_Modules

A web module, which contains one web page with static text. Entity: Cms_Static_Web_Modules

## Owner Tables Hierarchy

* [Cms_Web_Modules](Cms_Web_Modules.md)
* [Cms_Web_Sites](Cms_Web_Sites.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Static_Web_Module_Id](#static_web_module_id)|`uniqueidentifier` `PK`||
|[Web_Module_Id](#web_module_id)|`uniqueidentifier` |The web module, which is inherited by this static module.|
|[Language_Code](#language_code)|`nvarchar(7)` |The language code of the content.|
|[Content_Html](#content_html)|`nvarchar(2147483647)` |The actual html content of the pade. Only the <BODY> of the html is stored.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Static_Web_Module_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Web_Module_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Language_Code

| Property | Value |
| - | - |
|Type|nvarchar(7)|

### Content_Html

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


