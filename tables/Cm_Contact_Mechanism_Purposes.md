# Table Cm_Contact_Mechanism_Purposes

Contains user-defined purposes for processing contact mechanisms. Used for personal data management. Entity: Cm_Contact_Mechanism_Purposes (Introduced in version 18.2)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Contact_Mechanism_Purpose_Id](#contact_mechanism_purpose_id)|`uniqueidentifier` `PK`||
|[Code](#code)|`nvarchar(16)` ||
|[Name](#name)|`nvarchar(254)` `ML`|Name of the contact mechanism purpose (Multilanguage).|
|[Description](#description)|`nvarchar(2147483647)` ||
|[Contact_Mechanism_Type](#contact_mechanism_type)|`nvarchar(1)` Allowed: `A`, `E`, `F`, `M`, `O`, `T`, `W`|When specified, allows the purpose to be specified only for contact mechanisms of the specified type.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Contact_Mechanism_Purpose_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Contact_Mechanism_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


