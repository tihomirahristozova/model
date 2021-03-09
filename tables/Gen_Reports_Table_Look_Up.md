# Query Gen_Reports_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Report_Id](#report_id)|`uniqueidentifier` `PK`||
|[Report_Name](#report_name)|`nvarchar` ||
|[Query_Name](#query_name)|`nvarchar` |The name of the query or table that is used for root reference point of the loaded data.|
|[Is_Table](#is_table)|`bit` |If True the Query_Name is name of a table, otherwise is name of a query that can be filtered with Filter_Xml. |

## Columns

### Report_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Report_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Query_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Table

| Property | Value |
| - | - |
|Type|bit|


