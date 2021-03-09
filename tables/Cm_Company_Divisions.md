# Table Cm_Company_Divisions

Stores company divisions structure. The divisions are parties and as such, can be organized hierarchically mixed with other structuring mechanisms. The departments and divisions are parallel and different structuring mechanisms for the companies. Entity: Cm_Company_Divisions

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Company_Division_Id](#company_division_id)|`uniqueidentifier` `PK`|Company Division|
|[Party_Id](#party_id)|`uniqueidentifier` |The base party of the company division|
|[Company_Division_Code](#company_division_code)|`nvarchar(10)` |Company division code, unique within the company|
|[Company_Division_Name](#company_division_name)|`nvarchar(254)` `ML`|Multi-language company divsion name|
|[Company_Id](#company_id)|`uniqueidentifier` |The company to which this company division belongs|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Company_Division_Code

| Property | Value |
| - | - |
|Type|nvarchar(10)|

### Company_Division_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


