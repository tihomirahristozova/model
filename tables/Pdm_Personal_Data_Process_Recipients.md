# Table Pdm_Personal_Data_Process_Recipients

Contains recipients, to which personal data is disclosed. Entity: Pdm_Personal_Data_Process_Recipients (Introduced in version 18.2)

## Owner Tables Hierarchy

* [Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Personal_Data_Process_Recipient_Id](#personal_data_process_recipient_id)|`uniqueidentifier` `PK`||
|[Personal_Data_Process_Id](#personal_data_process_id)|`uniqueidentifier` |The process, whose data is disclosed to the recipient.|
|[Recipient_Party_Id](#recipient_party_id)|`uniqueidentifier` |The recipient, to whom the data is disclosed.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Personal_Data_Process_Recipient_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Personal_Data_Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Recipient_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


