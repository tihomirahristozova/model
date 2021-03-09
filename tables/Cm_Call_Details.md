# Table Cm_Call_Details

Contains call detail records. Calls are phone calls, video calls and SMS messages. Entity: Cm_Call_Details

## Summary

| Name | Type | Description |
| - | - | --- |
|[Call_Detail_Record_Id](#call_detail_record_id)|`uniqueidentifier` `PK`||
|[Start_Time](#start_time)|`datetime` |The starting date and time of the call|
|[Duration_Seconds](#duration_seconds)|`int` |The duration of the call (in seconds)|
|[Calling_Party_Number](#calling_party_number)|`nvarchar(80)` |The voice number of the originating party of the call|
|[Calling_Party_Id](#calling_party_id)|`uniqueidentifier` |The party, which originated the call.  NULL when the party was not determined successfully|
|[Called_Party_Number](#called_party_number)|`nvarchar(80)` |The voice number of the party, which received the call|
|[Called_Party_Id](#called_party_id)|`uniqueidentifier` |The party, which received the call. NULL when the party was not determined successfully|
|[Call_Unique_Id](#call_unique_id)|`nvarchar(32)` |The unique id of the call, as reported by the telephone central. NULL when the central did not report unique Id. Used for integration purposes|
|[External_Party_Id](#external_party_id)|`uniqueidentifier` |It is either the From or the To party - depending of the direction of the call. Only calls with at least one external party participating are usually logged. NULL when the respective party was null, or when no external party participated in the call|
|[External_Company_Id](#external_company_id)|`uniqueidentifier` |The company of the external party. It can be the party itself, or the parent party, whichever is company. NULL when the company cannot be determined|
|[Call_Type](#call_type)|`nvarchar(1)` Allowed: `P`, `V`, `M`|P=Phone; V=Video; M=Message/SMS|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Call_Detail_Record_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Start_Time

| Property | Value |
| - | - |
|Type|datetime|

### Duration_Seconds

| Property | Value |
| - | - |
|Type|int|

### Calling_Party_Number

| Property | Value |
| - | - |
|Type|nvarchar(80)|

### Calling_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Called_Party_Number

| Property | Value |
| - | - |
|Type|nvarchar(80)|

### Called_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Call_Unique_Id

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### External_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### External_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Call_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


