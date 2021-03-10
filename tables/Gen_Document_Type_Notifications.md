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


Document_Type_Notification_Id


.


.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Gen_Document_Type_Notifications](Gen_Document_Type_Notifications.md).[Document_Type_Notification_Id](Gen_Document_Type_Notifications.md#document_type_notification_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Document_Type_Id


Document_Type_Id


The document type for which this notification is set.


The document type for which this notification is set.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Type_Notifications](Gen_Document_Type_Notifications.md).[Document_Type_Id](Gen_Document_Type_Notifications.md#document_type_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Document_Event


Document_Event


The event which will trigger the notification


The event which will trigger the notification

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|StateChanging|
|Derived From|[Gen_Document_Type_Notifications](Gen_Document_Type_Notifications.md).[Document_Event](Gen_Document_Type_Notifications.md#document_event)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|254|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### State_Bit_Mask


State_Bit_Mask


The document states that will trigger the event


The document states that will trigger the event

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Gen_Document_Type_Notifications](Gen_Document_Type_Notifications.md).[State_Bit_Mask](Gen_Document_Type_Notifications.md#state_bit_mask)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### User_Status_Id


User_Status_Id


When not NULL, specifies that the event will be triggered only on this user status


When not NULL, specifies that the event will be triggered only on this user status

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Type_User_Statuses](Gen_Document_Type_User_Statuses.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Type_Notifications](Gen_Document_Type_Notifications.md).[User_Status_Id](Gen_Document_Type_Notifications.md#user_status_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Status_Change_Direction


Status_Change_Direction


Direction of status change. Positive when the new status is greater than the previous. Applicable values: Positive '+', Negative '-', No change '0', Any change '*'


Direction of status change. Positive when the new status is greater than the previous. Applicable values: Positive '+', Negative '-', No change '0', Any change '*'

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`*`, `0`, `+`, `-`|
|Default Value|*|
|Derived From|[Gen_Document_Type_Notifications](Gen_Document_Type_Notifications.md).[Status_Change_Direction](Gen_Document_Type_Notifications.md#status_change_direction)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|1|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Filter_XML


Filter_XML


Filtering condition for the document. Only documents which match the filter will trigger the event


Filtering condition for the document. Only documents which match the filter will trigger the event

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Type_Notifications](Gen_Document_Type_Notifications.md).[Filter_XML](Gen_Document_Type_Notifications.md#filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### To_Email_Address_List


To_Email_Address_List


List of email addressess to be notified


List of email addressess to be notified

| Property | Value |
| - | - |
|Type|nvarchar(2048)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Type_Notifications](Gen_Document_Type_Notifications.md).[To_Email_Address_List](Gen_Document_Type_Notifications.md#to_email_address_list)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2048|
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Type_Notifications](Gen_Document_Type_Notifications.md).[Row_Version](Gen_Document_Type_Notifications.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


