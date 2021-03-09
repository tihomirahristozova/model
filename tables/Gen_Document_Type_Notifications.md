# Table Gen_Document_Type_Notifications

Provides notification addresses to be notified upon occurrence of different document events. Entity: Gen_Document_Type_Notifications

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Type_Notification_Id](#document_type_notification_id)|`uniqueidentifier` `PK`|.|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type for which this notification is set.|
|[Document_Event](#document_event)|`nvarchar(254)` |The event which will trigger the notification|
|[State_Bit_Mask](#state_bit_mask)|`int` |The document states that will trigger the event|
|[User_Status_Id](#user_status_id)|`uniqueidentifier` |When not NULL, specifies that the event will be triggered only on this user status|
|[Status_Change_Direction](#status_change_direction)|`nvarchar(1)` Allowed: `*`, `0`, `+`, `-`|Direction of status change. Positive when the new status is greater than the previous. Applicable values: Positive '+', Negative '-', No change '0', Any change '*'|
|[Filter_XML](#filter_xml)|`nvarchar(2147483647)` |Filtering condition for the document. Only documents which match the filter will trigger the event|
|[To_Email_Address_List](#to_email_address_list)|`nvarchar(2048)` |List of email addressess to be notified|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Type_Notification_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Event

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### State_Bit_Mask

| Property | Value |
| - | - |
|Type|int|

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Status_Change_Direction

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Filter_XML

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### To_Email_Address_List

| Property | Value |
| - | - |
|Type|nvarchar(2048)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


