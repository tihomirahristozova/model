# Table Crm_Distribution_Channels

General list of distribution channels. Used to control prices and availability of products for the different channels. Entity: Crm_Distribution_Channels

## Summary

| Name | Type | Description |
| - | - | --- |
|[Distribution_Channel_Id](#distribution_channel_id)|`uniqueidentifier` `PK`||
|[Distribution_Channel_Code](#distribution_channel_code)|`nvarchar(10)` |Unique distribution channel code|
|[Distribution_Channel_Name](#distribution_channel_name)|`nvarchar(254)` `ML`|Multi-language name of the distribution channel|
|[Is_Active](#is_active)|`bit` |Is the channel active for new sales? 1=Yes, 0=No|
|[Description](#description)|`nvarchar(2147483647)` |Full description of the distribution channel|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Distribution_Channel_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Distribution_Channel_Code

| Property | Value |
| - | - |
|Type|nvarchar(10)|

### Distribution_Channel_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


