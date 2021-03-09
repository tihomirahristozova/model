# Table Fleet_Crews

Represents the crews, which can operate vehicles. Entity: Fleet_Crews

## Owner Tables Hierarchy

* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Crew_Id](#crew_id)|`uniqueidentifier` `PK`|Id of the crew|
|[Crew_Name](#crew_name)|`nvarchar(254)` `ML`|The name of the crew (multilanguage)|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company operating the crew|
|[Active](#active)|`bit` |Is the crew active? 1-active for choosing; 0-otherwise|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Crew_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Crew_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


