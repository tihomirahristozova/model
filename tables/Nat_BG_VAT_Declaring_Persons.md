# Table Nat_BG_VAT_Declaring_Persons

National data: Contains the persons, which are authorized to issue and sign VAT declarations. Entity: Nat_BG_VAT_Declaring_Persons

## Owner Tables Hierarchy

* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Declaring_Person_Id](#declaring_person_id)|`uniqueidentifier` `PK`|Unique identification of the declaring person.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company for which the person is presenting the declaration.|
|[Person_Id](#person_id)|`uniqueidentifier` |The person that is presenting the declaration.|
|[Declarer_Type](#declarer_type)|`nvarchar(1)` Allowed: `A`, `R`|Type of the declaring person. A=Attorney, R=Representative.|
|[Declaring_Person_City](#declaring_person_city)|`nvarchar(50)` |City from the address for correspondation of the declaring person.|
|[Declaring_Person_Postcode](#declaring_person_postcode)|`nvarchar(4)` |Postcode from the address for correspondation of the declaring person.|
|[Declaring_Person_Address](#declaring_person_address)|`nvarchar(150)` |Address for correspondation of the declaring person.|
|[Declaring_Person_Position](#declaring_person_position)|`nvarchar(50)` |Position of the declaring person in the enterprise company.|
|[Is_Default](#is_default)|`bit` |True if this is the default person, which issues VAT declarations for this Enterprise Company.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Declaring_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Declarer_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Declaring_Person_City

| Property | Value |
| - | - |
|Type|nvarchar(50)|

### Declaring_Person_Postcode

| Property | Value |
| - | - |
|Type|nvarchar(4)|

### Declaring_Person_Address

| Property | Value |
| - | - |
|Type|nvarchar(150)|

### Declaring_Person_Position

| Property | Value |
| - | - |
|Type|nvarchar(50)|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


