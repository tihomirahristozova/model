# Table Sec_Trusted_Application_Authorizations

Authorization of a trusted application to access the data on behalf of a context user. Entity: Sec_Trusted_Application_Authorizations (Introduced in version 20.1)

# Aggregate Hierarchy

* [Sec_Trusted_Applications](Sec_Trusted_Applications.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Trusted_Application_Authorization_Id|`Guid`|`PK`, Readonly||
|Grant_Time_Utc|`DateTime`||The time (in UTC) when the authorization was granted. `Required` `Default(NowUtc)` |
|Is_Revoked|`Boolean`||Specifies whether the grant is explicitly revoked. `Required` `Default(false)` |
|Notes|`String`||Notes for this TrustedApplicationAuthorization. |
|Valid_From_Utc|`DateTime?`||The start of the validitiy of the authorization. null means that there is no restriction. |
|Valid_Until_Utc|`DateTime?`||The time (in UTC) when the grant expires. null means that there is no time restriction. |
