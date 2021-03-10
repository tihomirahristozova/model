# Table Gen_Party_Location_Numbers

Location numbers for a party. Depending on the partner with which we are doing an exchange, our location number might be different. Entity: Gen_Party_Location_Numbers (Introduced in version 19.1)

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Party_Location_Number_Id](#party_location_number_id)|`uniqueidentifier` `PK`||
|[Party_Id](#party_id)|`uniqueidentifier` |The party for which we are defining the location number.|
|[Partner_Party_Id](#partner_party_id)|`uniqueidentifier` |The party with which we are doing exchange. Depending on the Partner Party, the main Party might have different location number. NULL means that the location number is not dependent on the Partner Party.|
|[Partner_Location_Number](#partner_location_number)|`nvarchar(16)` |The location number of the partner party for which we define the main Party location number. The location number of the main Party might be different depending on the location number of the partner party. NULL means that the location number is not dependent on the partner location number.|
|[Location_Coding_System](#location_coding_system)|`nvarchar(3)` Allowed: `GLN`, `INT`|The coding system for which we are defining the location number.|
|[Location_Number](#location_number)|`nvarchar(16)` |The location number of Party.|
|[Significance](#significance)|`int` |Order of significance of the location number within the main Party. If there are multiple location numbers, only the most significant is used. 0 is the least significant and higher numbers indicate higher significance.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Party_Location_Number_Id


Party_Location_Number_Id

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
|Derived From|[Gen_Party_Location_Numbers](Gen_Party_Location_Numbers.md).[Party_Location_Number_Id](Gen_Party_Location_Numbers.md#party_location_number_id)|
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


The party for which we are defining the location number.


The party for which we are defining the location number.

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
|Derived From|[Gen_Party_Location_Numbers](Gen_Party_Location_Numbers.md).[Party_Id](Gen_Party_Location_Numbers.md#party_id)|
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

### Partner_Party_Id


Partner_Party_Id


The party with which we are doing exchange. Depending on the Partner Party, the main Party might have different location number. NULL means that the location number is not dependent on the Partner Party.


The party with which we are doing exchange. Depending on the Partner Party, the main Party might have different location number. NULL means that the location number is not dependent on the Partner Party.

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
|Derived From|[Gen_Party_Location_Numbers](Gen_Party_Location_Numbers.md).[Partner_Party_Id](Gen_Party_Location_Numbers.md#partner_party_id)|
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

### Partner_Location_Number


Partner_Location_Number


The location number of the partner party for which we define the main Party location number. The location number of the main Party might be different depending on the location number of the partner party. NULL means that the location number is not dependent on the partner location number.


The location number of the partner party for which we define the main Party location number. The location number of the main Party might be different depending on the location number of the partner party. NULL means that the location number is not dependent on the partner location number.

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Party_Location_Numbers](Gen_Party_Location_Numbers.md).[Partner_Location_Number](Gen_Party_Location_Numbers.md#partner_location_number)|
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
|Max Length|16|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Location_Coding_System


Location_Coding_System


The coding system for which we are defining the location number.


The coding system for which we are defining the location number.

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`GLN`, `INT`|
|Default Value|GLN|
|Derived From|[Gen_Party_Location_Numbers](Gen_Party_Location_Numbers.md).[Location_Coding_System](Gen_Party_Location_Numbers.md#location_coding_system)|
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
|Max Length|3|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Location_Number


Location_Number


The location number of Party.


The location number of Party.

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Party_Location_Numbers](Gen_Party_Location_Numbers.md).[Location_Number](Gen_Party_Location_Numbers.md#location_number)|
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
|Max Length|16|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Significance


Significance


Order of significance of the location number within the main Party. If there are multiple location numbers, only the most significant is used. 0 is the least significant and higher numbers indicate higher significance.


Order of significance of the location number within the main Party. If there are multiple location numbers, only the most significant is used. 0 is the least significant and higher numbers indicate higher significance.

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
|Derived From|[Gen_Party_Location_Numbers](Gen_Party_Location_Numbers.md).[Significance](Gen_Party_Location_Numbers.md#significance)|
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
|GreaterThanOrLessThan|None|no|no|

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
|Derived From|[Gen_Party_Location_Numbers](Gen_Party_Location_Numbers.md).[Row_Version](Gen_Party_Location_Numbers.md#row_version)|
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


