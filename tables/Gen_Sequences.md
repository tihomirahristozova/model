# Table Gen_Sequences

Provides numbering sequences, applicable for use in a multi-threaded environment. Entity: Gen_Sequences

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sequence_Id](#sequence_id)|`uniqueidentifier` `PK`||
|[Sequence_Name](#sequence_name)|`nvarchar(50)` ||
|[Simultaneous_Transactions](#simultaneous_transactions)|`bit` |When false, specifies that the users will wait in a queue for a single numbering sequence generator. When true, the system will allow parallel numbering, by using any of the available sequence generators. However, parallel numbering has the drawback that, if no sequence generator is free, it will immediately throw exception, instead of waiting. So before setting to true, make sure that enough sequence generators are available.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sequence_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sequence_Name

| Property | Value |
| - | - |
|Type|nvarchar(50)|

### Simultaneous_Transactions

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


