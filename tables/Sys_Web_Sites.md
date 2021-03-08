# Table Sys_Web_Sites

Contains the web sites, which are hosted for the database. Entity: Sys_Web_Sites (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Web_Site_Id|`Guid`|`PK`, Readonly||
|Is_Active|`Boolean`||Indicates whether the web site is active and will be instantiated upon next web server restart. `Required` `Default(true)` `Filter(eq)` |
|Notes|`String`||Notes for this WebSite. |
|Relative_Url|`String`||The relative Url of the site. This is the text after the first slash after the protocol and host name. The text should not include the protocol and host name. null means that the site will be hosted as the root site in the speicified web host. |
|Web_Site_Type|`WebSiteType`|Allowed: `API`, `CC`, `ID`, `EC`, `LEG`, `SI`, `DM`, `PFL`, `APP`, `TAP`, `DAP`, `WMS`|The type of web site - Api, Client Center, Id, etc. `Required` `Filter(multi eq)` |
