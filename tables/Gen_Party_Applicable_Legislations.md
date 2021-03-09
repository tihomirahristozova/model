# Table Gen_Party_Applicable_Legislations

Specifies a legislation, which is applicable for a party. A single party can have more than one applicable legislations. Entity: Gen_Party_Applicable_Legislations (Introduced in version 19.1)

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Party_Applicable_Legislation_Id](#party_applicable_legislation_id)|`uniqueidentifier` `PK`||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Applicable_Legislation](#applicable_legislation)|`nvarchar(8)` Allowed: `AE`, `AU`, `BG`, `CA`, `CN`, `CZ`, `DE`, `ES`, `EU`, `FR`, `GR`, `HU`, `IN`, `IT`, `JP`, `MK`, `PL`, `PT`, `RO`, `RS`, `RU`, `TR`, `UK`, `US`, `ZA`|A legislation, which applies to the specified party. The list of legislations is system defined, and contains legislations for which system rules are currently defined. For example: US, UK, EU, DE, FR, ES, IT, BG, MK, RO, GR, etc.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Party_Applicable_Legislation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Applicable_Legislation

| Property | Value |
| - | - |
|Type|nvarchar(8)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


