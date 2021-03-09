# Table Crm_Sales_Persons

Sales persons (or representatives) are sellers inside the enterprise company who sell the products to customers. Entity: Crm_Sales_Persons

## Owner Tables Hierarchy

* [Cm_Persons](Cm_Persons.md)
* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` `PK`|Unique sales person Id|
|[Person_Id](#person_id)|`uniqueidentifier` |Base personal record|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Commission_Policy_Id](#commission_policy_id)|`uniqueidentifier` |Current commission policy for the sales person. NULL means there is no commission policy|
|[Commission_Percent](#commission_percent)|`decimal(7, 6)` |The percentage (0..1) of commission percent. NULL means that there is no commission percent.|
|[Sales_Person_Group_Id](#sales_person_group_id)|`uniqueidentifier` |The sales person group to which this sales person is assigned.|
|[Contract_Start_Date](#contract_start_date)|`datetime` |The starting date of the contract with the sales person. NULL when it is unknown.|
|[Contract_End_Date](#contract_end_date)|`datetime` |The ending date of the contract with the sales person. NULL when the sales person is still active.|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location, to which the sales person is assigned. The sales person is allowed to sell to other locations, but this is the default location. NULL means that the sales person is not assigned to any enterprise location.|
|[Is_Active](#is_active)|`bit` |Specifies whether the sales person is active and should be included in the list when choosing sales person through drop-downs, lists, etc.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Commission_Policy_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Commission_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Sales_Person_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Contract_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Contract_End_Date

| Property | Value |
| - | - |
|Type|datetime|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


