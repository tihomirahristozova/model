# Table Crm_Distribution_Channels

General list of distribution channels. Used to control prices and availability of products for the different channels. Entity: Crm_Distribution_Channels

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Distribution_Channel_Id|`Guid`|`PK`, Readonly||
|Distribution_Channel_Code|`String`||Unique distribution channel code. `Required` `Filter(eq;like)` |
|Description|`String`||Full description of the distribution channel. |
|Is_Active|`Boolean`||Is the channel active for new sales? true=Yes, false=No. `Required` `Default(true)` `Filter(eq)` |
|Distribution_Channel_Name|`MultilanguageString`||Multi-language name of the distribution channel. `Required` `Filter(eq;like)` |
