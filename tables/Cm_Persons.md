# Table Cm_Persons

Personal records. Requires related party record. Entity: Cm_Persons

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Person_Id](#person_id)|`uniqueidentifier` `PK`|Unique person Id|
|[First_Name](#first_name)|`nvarchar(64)` `ML`|First name of the person.|
|[Middle_Name](#middle_name)|`nvarchar(64)` `ML`|Middle name of the person.|
|[Last_Name](#last_name)|`nvarchar(64)` `ML`|Last name of the person.|
|[Title](#title)|`nvarchar(32)` `ML`|The persons title. It may be one of the standard titles - Mr., Mrs., etc., but it can also contains professional or academic qualification.|
|[Gender](#gender)|`nvarchar(1)` Allowed: `F`, `M`|Person gender. M=Male;F=Female;NULL=not known/not provided|
|[Birth_Date](#birth_date)|`datetime` |Birth date. NULL means unknown|
|[Nationality](#nationality)|`uniqueidentifier` |Person's nationality. NULL means the default (same as enterprise) nationality|
|[National_Number](#national_number)|`nvarchar(14)` |Government assigned unique personal number. NULL means unknown|
|[Passport_Number](#passport_number)|`nvarchar(14)` |Current passport number. NULL means unknown|
|[Passport_Issuing_Date](#passport_issuing_date)|`datetime` |Date of issuing the passport. NULL means unknown|
|[City](#city)|`nvarchar(64)` `ML`|City from the legal registration address for the person|
|[Notes](#notes)|`nvarchar(254)` |Internal notes for the person|
|[Update_User](#update_user)|`nvarchar(64)` Readonly||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar(64)` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Party_Id](#party_id)|`uniqueidentifier` |The Id of the party record for this person. The party stores the person's full name|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### First_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Middle_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Last_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Title

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Gender

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Birth_Date

| Property | Value |
| - | - |
|Type|datetime|

### Nationality

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### National_Number

| Property | Value |
| - | - |
|Type|nvarchar(14)|

### Passport_Number

| Property | Value |
| - | - |
|Type|nvarchar(14)|

### Passport_Issuing_Date

| Property | Value |
| - | - |
|Type|datetime|

### City

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

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

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


