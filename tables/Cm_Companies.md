# Table Cm_Companies

Contains company definitions. Entity: Cm_Companies

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Company_Id](#company_id)|`uniqueidentifier` `PK`|Unique company Id|
|[Party_Id](#party_id)|`uniqueidentifier` |Base party Id|
|[Company_Name](#company_name)|`nvarchar(254)` `ML`||
|[Registration_Type](#registration_type)|`nvarchar(16)` `ML`|Legal registration type - like LTD., PLC, etc. NULL means unknown|
|[Registration_Primary_Address](#registration_primary_address)|`nvarchar(254)` `ML`|The primary registration address of the company.|
|[Registration_Number](#registration_number)|`nvarchar(16)` |Unique, government-assigned registration number. NULL means unknown|
|[Country_Id](#country_id)|`uniqueidentifier` |The country, where the company is registered.|
|[Is_VAT_Registered](#is_vat_registered)|`bit` |Determines wheather the company is included in VAT registers.|
|[Registration_VAT_Number](#registration_vat_number)|`nvarchar(16)` |VAT registration number where applicable. NULL means that VAT number is not applicable or unknown|
|[Responsible_Person_Name](#responsible_person_name)|`nvarchar(64)` `ML`|Primary responsible person of the company. NULL means unknown.|
|[Registration_Responsible_Person_Id](#registration_responsible_person_id)|`uniqueidentifier` |The personal record of the primary responsible person as per registration. NULL means unknown|
|[Branch_Number](#branch_number)|`int` |Branch number of the company. Companies with equal names and/or registration numbers can be inserted only if their branch numbers are different.|
|[City](#city)|`nvarchar(64)` `ML`|The city in which the company is registered.|
|[Is_VAT_Cash_Reporting_Registered](#is_vat_cash_reporting_registered)|`bit` |When true, specifies that the company uses the special VAT Cash Reporting Mode.|
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar(64)` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar(64)` Readonly||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Company_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Registration_Type

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Registration_Primary_Address

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Registration_Number

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_VAT_Registered

| Property | Value |
| - | - |
|Type|bit|

### Registration_VAT_Number

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Responsible_Person_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Registration_Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Branch_Number

| Property | Value |
| - | - |
|Type|int|

### City

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Is_VAT_Cash_Reporting_Registered

| Property | Value |
| - | - |
|Type|bit|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


