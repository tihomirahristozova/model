# Query Sec_Access_Keys_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` `PK`||
|[Access_Key_Code](#access_key_code)|`nvarchar` |Unique code for the access key. The codes can be null for legacy keys or entities that do not support codes. The codes are unique only among non-null entries|
|[Access_Key_Name](#access_key_name)|`nvarchar` `ML`|Multilanguage descriptive name of the security key. Can be null for legacy keys|
|[Entity_Name](#entity_name)|`nvarchar` |What entitity the key secures. Can be null for private, legacy keys|

## Columns

### Access_Key_Id


Access_Key_Id

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
|Derived From|[Sec_Access_Keys](Sec_Access_Keys.md).[Access_Key_Id](Sec_Access_Keys.md#access_key_id)|
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
|Equals|NULL|no|no|

### Access_Key_Code


Access_Key_Code


Unique code for the access key. The codes can be null for legacy keys or entities that do not support codes. The codes are unique only among non-null entries


Unique code for the access key. The codes can be null for legacy keys or entities that do not support codes. The codes are unique only among non-null entries

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Access_Keys](Sec_Access_Keys.md).[Access_Key_Code](Sec_Access_Keys.md#access_key_code)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Access_Key_Name


Access_Key_Name


Multilanguage descriptive name of the security key. Can be null for legacy keys


Multilanguage descriptive name of the security key. Can be null for legacy keys

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Access_Keys](Sec_Access_Keys.md).[Access_Key_Name](Sec_Access_Keys.md#access_key_name)|
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
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Entity_Name


Entity_Name


What entitity the key secures. Can be null for private, legacy keys


What entitity the key secures. Can be null for private, legacy keys

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Access_Keys](Sec_Access_Keys.md).[Entity_Name](Sec_Access_Keys.md#entity_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|yes|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|


