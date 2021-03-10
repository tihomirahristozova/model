# Table Log_Transportation_Modes

Represents a mode of transportation, like water, air, road, etc. Entity: Log_Transportation_Modes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transportation_Mode_Id](#transportation_mode_id)|`uniqueidentifier` `PK`||
|[Transportation_Mode_Code](#transportation_mode_code)|`nvarchar(8)` |Unique transportation mode code.|
|[Transportation_Mode_Name](#transportation_mode_name)|`nvarchar(254)` |Multilanguage name of the mode of transportation.|
|[System_Icon](#system_icon)|`nvarchar(1)` |Icon, depicting the mode of transport. A=Air, W=Water, T=Train/Rail, R=Road, O=Other.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Transportation_Mode_Id


Transportation_Mode_Id

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
|Derived From|[Log_Transportation_Modes](Log_Transportation_Modes.md).[Transportation_Mode_Id](Log_Transportation_Modes.md#transportation_mode_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Transportation_Mode_Code


Transportation_Mode_Code


Unique transportation mode code.


Unique transportation mode code.

| Property | Value |
| - | - |
|Type|nvarchar(8)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Log_Transportation_Modes](Log_Transportation_Modes.md).[Transportation_Mode_Code](Log_Transportation_Modes.md#transportation_mode_code)|
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
|Max Length|8|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Transportation_Mode_Name


Transportation_Mode_Name


Multilanguage name of the mode of transportation.


Multilanguage name of the mode of transportation.

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
|Default Value|None|
|Derived From|[Log_Transportation_Modes](Log_Transportation_Modes.md).[Transportation_Mode_Name](Log_Transportation_Modes.md#transportation_mode_name)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### System_Icon


System_Icon


Icon, depicting the mode of transport. A=Air, W=Water, T=Train/Rail, R=Road, O=Other.


Icon, depicting the mode of transport. A=Air, W=Water, T=Train/Rail, R=Road, O=Other.

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
|Default Value|O|
|Derived From|[Log_Transportation_Modes](Log_Transportation_Modes.md).[System_Icon](Log_Transportation_Modes.md#system_icon)|
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
|Max Length|1|
|Order|2147483647|
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
|Derived From|[Log_Transportation_Modes](Log_Transportation_Modes.md).[Row_Version](Log_Transportation_Modes.md#row_version)|
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


