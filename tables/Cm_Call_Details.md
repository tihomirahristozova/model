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


Call_Detail_Record_Id

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
|Derived From|[Cm_Call_Details](Cm_Call_Details.md).[Call_Detail_Record_Id](Cm_Call_Details.md#call_detail_record_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Start_Time


Start_Time


The starting date and time of the call


The starting date and time of the call

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Call_Details](Cm_Call_Details.md).[Start_Time](Cm_Call_Details.md#start_time)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Duration_Seconds


Duration_Seconds


The duration of the call (in seconds)


The duration of the call (in seconds)

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
|Derived From|[Cm_Call_Details](Cm_Call_Details.md).[Duration_Seconds](Cm_Call_Details.md#duration_seconds)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Calling_Party_Number


Calling_Party_Number


The voice number of the originating party of the call


The voice number of the originating party of the call

| Property | Value |
| - | - |
|Type|nvarchar(80)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Call_Details](Cm_Call_Details.md).[Calling_Party_Number](Cm_Call_Details.md#calling_party_number)|
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
|Max Length|80|
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

### Calling_Party_Id


Calling_Party_Id


The party, which originated the call.  NULL when the party was not determined successfully


The party, which originated the call.  NULL when the party was not determined successfully

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Call_Details](Cm_Call_Details.md).[Calling_Party_Id](Cm_Call_Details.md#calling_party_id)|
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
|Equals|NULL|yes|no|

### Called_Party_Number


Called_Party_Number


The voice number of the party, which received the call


The voice number of the party, which received the call

| Property | Value |
| - | - |
|Type|nvarchar(80)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Call_Details](Cm_Call_Details.md).[Called_Party_Number](Cm_Call_Details.md#called_party_number)|
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
|Max Length|80|
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

### Called_Party_Id


Called_Party_Id


The party, which received the call. NULL when the party was not determined successfully


The party, which received the call. NULL when the party was not determined successfully

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Call_Details](Cm_Call_Details.md).[Called_Party_Id](Cm_Call_Details.md#called_party_id)|
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
|Equals|NULL|yes|no|

### Call_Unique_Id


Call_Unique_Id


The unique id of the call, as reported by the telephone central. NULL when the central did not report unique Id. Used for integration purposes


The unique id of the call, as reported by the telephone central. NULL when the central did not report unique Id. Used for integration purposes

| Property | Value |
| - | - |
|Type|nvarchar(32)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Call_Details](Cm_Call_Details.md).[Call_Unique_Id](Cm_Call_Details.md#call_unique_id)|
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
|Max Length|32|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### External_Party_Id


External_Party_Id


It is either the From or the To party - depending of the direction of the call. Only calls with at least one external party participating are usually logged. NULL when the respective party was null, or when no external party participated in the call


It is either the From or the To party - depending of the direction of the call. Only calls with at least one external party participating are usually logged. NULL when the respective party was null, or when no external party participated in the call

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Call_Details](Cm_Call_Details.md).[External_Party_Id](Cm_Call_Details.md#external_party_id)|
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
|Equals|NULL|yes|no|

### External_Company_Id


External_Company_Id


The company of the external party. It can be the party itself, or the parent party, whichever is company. NULL when the company cannot be determined


The company of the external party. It can be the party itself, or the parent party, whichever is company. NULL when the company cannot be determined

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Companies](Cm_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Call_Details](Cm_Call_Details.md).[External_Company_Id](Cm_Call_Details.md#external_company_id)|
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
|Equals|NULL|yes|no|

### Call_Type


Call_Type


P=Phone; V=Video; M=Message/SMS


P=Phone; V=Video; M=Message/SMS

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
|Allowed Values|`P`, `V`, `M`|
|Default Value|P|
|Derived From|[Cm_Call_Details](Cm_Call_Details.md).[Call_Type](Cm_Call_Details.md#call_type)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

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
|Derived From|[Cm_Call_Details](Cm_Call_Details.md).[Row_Version](Cm_Call_Details.md#row_version)|
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


