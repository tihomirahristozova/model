# Table Gen_Config

Hierarchical repository of configuration options. Entity: Gen_Config

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Config_Id|`Guid`|`PK`, Readonly||
|Description|`String`||The description of this Config. |
|Is_Active|`Boolean`||Indicates whether this config entry is active. Inactive config entries are not taken into account. `Required` `Default(true)` `Filter(eq)` `Introduced in version 19.1` |
|Key_Path|`String`||Full path of the configuration option. `Required` `Filter(eq)` `ORD` |
|Key_Value|`String`||The value of the configuration option. |
|User_Login|`String`||If not null, the configuration option is specific to the user. `Filter(eq)` |
|User_Machine|`String`||If not null, the configuration option is specific to the machine. `Filter(eq)` |
