# Table Cm_Company_Locations

Stores company locations. The locations are parties and as such, can be organized hierarchically mixed with other structuring mechanisms. The locations, departments and divisions are parallel and different structuring mechanisms for the companies. Entity: Cm_Company_Locations

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Company_Location_Id](#company_location_id)|`uniqueidentifier` `PK`||
|[Party_Id](#party_id)|`uniqueidentifier` |The party of the company location.|
|[Company_Id](#company_id)|`uniqueidentifier` |The company to which this location belongs.|
|[Location_Name](#location_name)|`nvarchar(64)` `ML`|The name of the company location.|
|[Working_Time](#working_time)|`nvarchar(254)` |Textual representation of the working time of the location.|
|[Bill_To](#bill_to)|`nvarchar(1)` Allowed: `C`, `L`|If filled indicates which party is billed for the amounts from documents that require payments. This setting is used in CRM module when the company and the location are customers. Possible values: 'C' = Company, 'L' = Company location, NULL = unidentified|
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Location_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Working_Time

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Bill_To

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


