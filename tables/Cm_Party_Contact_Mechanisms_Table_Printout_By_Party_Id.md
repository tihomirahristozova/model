# Procedure Cm_Party_Contact_Mechanisms_Table_Printout_By_Party_Id


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique party contact mechanism Id|
|[Party_Id](#party_id)|`uniqueidentifier` |The party, having the contact mechanism|
|[Party_Name](#party_name)|`nvarchar` `ML`|The name of the party|
|[Contact_Mechanism_Id](#contact_mechanism_id)|`uniqueidentifier` |The contact mechanism of the party|
|[Contact_Mechanism_Name](#contact_mechanism_name)|`nvarchar` |Contact mechanism description|
|[Contact_Mechanism_Type](#contact_mechanism_type)|`nvarchar` Allowed: `A`, `E`, `F`, `M`, `O`, `T`, `W`|A=Address; E=e-mail; T=Telephone|
|[From_Date](#from_date)|`datetime` |The first date when the contact mechanism was valid. NULL means unknown date|
|[Thru_Date](#thru_date)|`datetime` |The last date on which the contact mechanism was valid for the party. NULL if the contact mechanism is still valid|
|[Non_Solicitation](#non_solicitation)|`bit` |If 1 then Don't use the mechanism for solicitation purposes|
|[Notes](#notes)|`nvarchar` ||
|[Is_Default](#is_default)|`bit` |1 - when this is the default contact mechanism for this party; 0 - otherwise|
|[Is_Active](#is_active)|`bit` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Contact_Mechanism_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Contact_Mechanism_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Contact_Mechanism_Type

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|


