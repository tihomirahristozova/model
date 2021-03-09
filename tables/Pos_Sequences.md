# Table Pos_Sequences

Stores the last issued fiscal sales number for each POS device. Entity: Pos_Sequences (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Pos_Sequence_Id](#pos_sequence_id)|`uniqueidentifier` `PK`||
|[Pos_Device_Id](#pos_device_id)|`uniqueidentifier` |The POS device, for which the sequence is defined.|
|[Next_No](#next_no)|`nvarchar(16)` |The next consecutive number which will be assigned on the next request.|
|[Max_No](#max_no)|`nvarchar(16)` |Specifies the maximum number allowed in the sequence. NULL means that the sequence will grow unlimited.|
|[Row_Version](#row_version)|`timestamp` ||
|[Is_Active](#is_active)|`bit` |Indicates whether this sequence is active.|

## Columns

### Pos_Sequence_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Device_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Next_No

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Max_No

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|


