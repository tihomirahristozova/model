# Table Cms_Web_Sites

Contains the public web sites. Entity: Cms_Web_Sites

## Summary

| Name | Type | Description |
| - | - | --- |
|[Web_Site_Id](#web_site_id)|`uniqueidentifier` `PK`||
|[Web_Site_Name](#web_site_name)|`nvarchar(256)` |Multilanguage web site name|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company to which this web site belongs.|
|[Base_Url](#base_url)|`nvarchar(256)` |The base url (address) of the web site.|
|[Public_User_List_Id](#public_user_list_id)|`uniqueidentifier` |The list of users used to authorize the users on the site.|
|[Is_Published](#is_published)|`bit` |Specifies whether the site is published for public Internet access.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Web_Site_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Web_Site_Name

| Property | Value |
| - | - |
|Type|nvarchar(256)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Base_Url

| Property | Value |
| - | - |
|Type|nvarchar(256)|

### Public_User_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Published

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


