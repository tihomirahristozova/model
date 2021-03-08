# Table Gen_Document_Type_Notifications

Provides notification addresses to be notified upon occurrence of different document events. Entity: Gen_Document_Type_Notifications

# Aggregate Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Type_Notification_Id|`Guid`|`PK`, Readonly||
|Document_Event|`String`||The event which will trigger the notification. `Required` `Default("StateChanging")` `Filter(eq)` |
|Filter_XML|`String`||Filtering condition for the document. Only documents which match the filter will trigger the event. |
|State_Bit_Mask|`Int32`||The document states that will trigger the event. `Required` `Default(0)` |
|Status_Change_Direction|`StatusChangeDirection`|Allowed: `*`, `0`, `+`, `-`|Direction of status change. Positive when the new status is greater than the previous. Applicable values: Positive '+', Negative '-', No change '0', Any change '*'. `Required` `Default("*")` |
|To_Email_Address_List|`String`||List of email addressess to be notified. `Required` |
