# Table Cms_Web_Site_Languages

Specifies a language, supported by the web site. Entity: Cms_Web_Site_Languages

## Owner Tables Hierarchy

* [Cms_Web_Sites](Cms_Web_Sites.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Web_Site_Language_Id](#web_site_language_id)|`uniqueidentifier` `PK`||
|[Web_Site_Id](#web_site_id)|`uniqueidentifier` |The web site, for which the language is specified.|
|[Language_Code](#language_code)|`nvarchar(2)` |Two letter ISO language code. Sub-tags are currently not supported.|
|[Is_Active](#is_active)|`bit` |Specifies whether the support for the language is activated and should be published on the web.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Web_Site_Language_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Web_Site_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Language_Code

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


