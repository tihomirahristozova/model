# Table Sec_Access_Keys

Access keys provide the basic locking mechanism for data security. Each record can be secured by specifying an access key. Then the users are given access to access keys through groups. Entity: Sec_Access_Keys

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Access_Key_Id|`Guid`|`PK`, Readonly||
|Access_Key_Code|`String`||Unique code for the access key. The codes can be null for legacy keys or entities that do not support codes. The codes are unique only among non-null entries. `Filter(eq;like)` |
|Entity_Name|`String`||What entitity the key secures. Can be null for private, legacy keys. `Filter(eq;like)` `ORD` |
|Access_Key_Name|`MultilanguageString`||Multilanguage descriptive name of the security key. Can be null for legacy keys. `Filter(eq;like)` |
