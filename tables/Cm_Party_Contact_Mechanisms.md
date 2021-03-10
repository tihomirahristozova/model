# Table Cm_Party_Contact_Mechanisms

Specifies the contact mechanisms, which are attached to the parties. Currently each contact mechanism is attached to strictly one party. Entity: Cm_Party_Contact_Mechanisms

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique party contact mechanism Id|
|[Party_Id](#party_id)|`uniqueidentifier` |The party, having the contact mechanism|
|[Contact_Mechanism_Id](#contact_mechanism_id)|`uniqueidentifier` |The contact mechanism of the party|
|[From_Date](#from_date)|`datetime` |The first date when the contact mechanism was valid. NULL means unknown date|
|[Thru_Date](#thru_date)|`datetime` |The last date on which the contact mechanism was valid for the party. NULL if the contact mechanism is still valid|
|[Non_Solicitation](#non_solicitation)|`bit` |If 1 then Don't use the mechanism for solicitation purposes|
|[Notes](#notes)|`nvarchar(254)` ||
|[Is_Default](#is_default)|`bit` |1 - when this is the default contact mechanism for this party; 0 - otherwise|
|[Is_Active](#is_active)|`bit` |True if the contact mechanism is currently active and can be used to contact the party.|
|[Line_Ord](#line_ord)|`int` |Consecutive number of the contact information. The number is unique within the party.|
|[Row_Version](#row_version)|`timestamp` ||
|[Contact_Mechanism_Purpose_Id](#contact_mechanism_purpose_id)|`uniqueidentifier` |The purpose of this contact mechanism. Unique within the party. Can be used to seek for specific contact mechanisms.|
|[Personal_Data_Process_Id](#personal_data_process_id)|`uniqueidentifier` |The personal data process, which is used to process the current data. Null when the data is not personal or when the process is unknown.|

## Columns

### Id


Id


Unique party contact mechanism Id


Unique party contact mechanism Id

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
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[Id](Cm_Party_Contact_Mechanisms.md#id)|
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
|Equals|NULL|no|no|

### Party_Id


Party_Id


The party, having the contact mechanism


The party, having the contact mechanism

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[Party_Id](Cm_Party_Contact_Mechanisms.md#party_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Contact_Mechanism_Id


Contact_Mechanism_Id


The contact mechanism of the party


The contact mechanism of the party

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Contact_Mechanisms](Cm_Contact_Mechanisms.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[Contact_Mechanism_Id](Cm_Party_Contact_Mechanisms.md#contact_mechanism_id)|
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
|Equals|NULL|no|no|

### From_Date


From_Date


The first date when the contact mechanism was valid. NULL means unknown date


The first date when the contact mechanism was valid. NULL means unknown date

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDate|
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[From_Date](Cm_Party_Contact_Mechanisms.md#from_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Thru_Date


Thru_Date


The last date on which the contact mechanism was valid for the party. NULL if the contact mechanism is still valid


The last date on which the contact mechanism was valid for the party. NULL if the contact mechanism is still valid

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[Thru_Date](Cm_Party_Contact_Mechanisms.md#thru_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Non_Solicitation


Non_Solicitation


If 1 then Don't use the mechanism for solicitation purposes


If 1 then Don't use the mechanism for solicitation purposes

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[Non_Solicitation](Cm_Party_Contact_Mechanisms.md#non_solicitation)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[Notes](Cm_Party_Contact_Mechanisms.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

### Is_Default


Is_Default


1 - when this is the default contact mechanism for this party; 0 - otherwise


1 - when this is the default contact mechanism for this party; 0 - otherwise

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[Is_Default](Cm_Party_Contact_Mechanisms.md#is_default)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Is_Active


Is_Active


True if the contact mechanism is currently active and can be used to contact the party.


True if the contact mechanism is currently active and can be used to contact the party.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[Is_Active](Cm_Party_Contact_Mechanisms.md#is_active)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Line_Ord


Line_Ord


Consecutive number of the contact information. The number is unique within the party.


Consecutive number of the contact information. The number is unique within the party.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|1|
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[Line_Ord](Cm_Party_Contact_Mechanisms.md#line_ord)|
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
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[Row_Version](Cm_Party_Contact_Mechanisms.md#row_version)|
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

### Contact_Mechanism_Purpose_Id


Contact_Mechanism_Purpose_Id


The purpose of this contact mechanism. Unique within the party. Can be used to seek for specific contact mechanisms.


The purpose of this contact mechanism. Unique within the party. Can be used to seek for specific contact mechanisms.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Contact_Mechanism_Purposes](Cm_Contact_Mechanism_Purposes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[Contact_Mechanism_Purpose_Id](Cm_Party_Contact_Mechanisms.md#contact_mechanism_purpose_id)|
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

### Personal_Data_Process_Id


Personal_Data_Process_Id


The personal data process, which is used to process the current data. Null when the data is not personal or when the process is unknown.


The personal data process, which is used to process the current data. Null when the data is not personal or when the process is unknown.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md).[Personal_Data_Process_Id](Cm_Party_Contact_Mechanisms.md#personal_data_process_id)|
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


