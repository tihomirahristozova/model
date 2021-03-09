# Query Nat_BG_VAT_Declaring_Persons_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Declaring_Person_Id](#declaring_person_id)|`uniqueidentifier` `PK`|Unique identification of the declaring person.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company for which the person is presenting the declaration.|
|[Person_Id](#person_id)|`uniqueidentifier` |The person that is presenting the declaration.|
|[Declarer_Type](#declarer_type)|`nvarchar` Allowed: `A`, `R`|Type of the declaring person. A=Attorney, R=Representative.|
|[Declaring_Person_City](#declaring_person_city)|`nvarchar` |City from the address for correspondation of the declaring person.|
|[Declaring_Person_Postcode](#declaring_person_postcode)|`nvarchar` |Postcode from the address for correspondation of the declaring person.|
|[Declaring_Person_Address](#declaring_person_address)|`nvarchar` |Address for correspondation of the declaring person.|
|[Declaring_Person_Position](#declaring_person_position)|`nvarchar` |Position of the declaring person in the enterprise company.|
|[Is_Default](#is_default)|`bit` |True if this is the default person, which issues VAT declarations for this Enterprise Company.|

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
|Type|nvarchar|

### Declaring_Person_City

| Property | Value |
| - | - |
|Type|nvarchar|

### Declaring_Person_Postcode

| Property | Value |
| - | - |
|Type|nvarchar|

### Declaring_Person_Address

| Property | Value |
| - | - |
|Type|nvarchar|

### Declaring_Person_Position

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|


