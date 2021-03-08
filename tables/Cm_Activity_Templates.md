# Table Cm_Activity_Templates

Templates for automatical generation of activity from any document. Entity: Cm_Activity_Templates

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Activity_Template_Id|`Guid`|`PK`, Readonly||
|Activity_Subject_Mask|`String`||A mask that uses fields from the header table of the source document in the specified route and is used to fill the Subject of the generated activity. |
|Additional_Days|`Int32`||The number of days that will be added to the date in the Header_Date_Field. The result value is set to Start_Time of the activity. `Required` `Default(0)` |
|Reminder_Time|`TimeSpan?`||Time of the day for the reminder. |
|Source_Date_Field|`String`||A name of a field from the header or the document table of the source document in the specified route, that will be used along with Additional_Days to set the Start_Time of the generated activity. `Required` |
|Start_Time|`TimeSpan`||The time of the day when the activity starts. `Required` |
