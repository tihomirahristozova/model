# Table Cm_Party_Contact_Mechanisms

Specifies the contact mechanisms, which are attached to the parties. Currently each contact mechanism is attached to strictly one party. Entity: Cm_Party_Contact_Mechanisms

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique party contact mechanism Id|
|[Party_Id](#party_id)|`uniqueidentifier` |The party, having the contact mechanism|
|[Contact_Mechanism_Id](#contact_mechanism_id)|`uniqueidentifier` |The contact mechanism of the party|
|[From_Date](#from_date)|`datetime` |The first date when the contact mechanism was valid. NULL means unknown date|
|[Thru_Date](#thru_date)|`datetime` |The last date on which the contact mechanism was valid for the party. NULL if the contact mechanism is still valid|
|[Non_Solicitation](#non_solicitation)|`bit` |If 1 then Don't use the mechanism for solicitation purposes|
|[Notes](#notes)|`nvarchar(254)` ||
|[Is_Default](#is_default)|`bit` |1 - when this is the default contact mechanism for this party; 0 - otherwise|
|[Is_Active](#is_active)|`bit` |True if the contact mechanism is currently active and can be used to contact the party.|
|[Line_Ord](#line_ord)|`int` |Consecutive number of the contact information. The number is unique within the party.|
|[Row_Version](#row_version)|`timestamp` ||
|[Contact_Mechanism_Purpose_Id](#contact_mechanism_purpose_id)|`uniqueidentifier` |The purpose of this contact mechanism. Unique within the party. Can be used to seek for specific contact mechanisms.|
|[Personal_Data_Process_Id](#personal_data_process_id)|`uniqueidentifier` |The personal data process, which is used to process the current data. Null when the data is not personal or when the process is unknown.|

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Contact_Mechanism_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Thru_Date

| Property | Value |
| - | - |
|Type|datetime|

### Non_Solicitation

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Contact_Mechanism_Purpose_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Personal_Data_Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


