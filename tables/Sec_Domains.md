# Table Sec_Domains

Represents one user domain. The users in a domain have different emails. But one user can use the same email to register in different domains. Entity: Sec_Domains (Introduced in version 20.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Domain_Id|`Guid`|`PK`, Readonly||
|Allow_Local_Accounts|`Boolean`||Specifies whether users can have local accounts with locally stored passwords in the DB (not recommended). `Required` `Default(true)` |
|Description|`MultilanguageString`||Multi-language description of the domain. |
|Is_Default|`Boolean`||Specifies whether this is the default domain for the database. `Required` `Default(true)` `Filter(eq)` |
|Domain_Name|`String`||The name of the domain (restricted for URL usage). `Required` `Filter(eq;like)` `ORD` |
