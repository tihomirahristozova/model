# Table Sys_Web_Hosts

Contains the names and https certificates of the different host names used to host sites. Entity: Sys_Web_Hosts (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Web_Host_Id|`Guid`|`PK`, Readonly||
|Certificate_Contents|`Byte[]`|`BLOB`|The contents of the web host certificate. null means to use the server system certificate. |
|Certificate_Expiry_Date|`DateTime?`||The expiry date of the certificate. Can be used to track the expiration of the web host certificates. When null, the expiry date was not provided by the user, when uploading the certificate. `Filter(multi eq)` |
|Certificate_Original_Filename|`String`||The original name of the file, used to upload the certificate. Used only for reference purposes. When null, means that the user did not provide that information when uploading the certificate. `Filter(eq;like)` |
|Certificate_Password|`String`||The password, which should be used to decrypt the certificate. null when the certificate has no password or the system certificate is used. |
|Certificate_Type|`String`||The type of certificate uploaded. Currently, only PFX is supported. `Required` `Default("PFX")` `Filter(multi eq)` |
|Web_Host_Name|`String`||The unique Internet name of the host. Should NOT include protocol name and should NOT include any forward slashes. This is just the dot-separated host name. `Required` `Filter(multi eq;like)` |
|Notes|`String`||Notes for this WebHost. |
