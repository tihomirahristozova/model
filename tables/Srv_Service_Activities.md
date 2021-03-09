# Table Srv_Service_Activities

Contains service activity headers. The service activities are the actual actions performed to service (repair) an object. Entity: Srv_Service_Activities

## Owner Tables Hierarchy

* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Service_Activity_Id](#service_activity_id)|`uniqueidentifier` `PK`||
|[Activity_Id](#activity_id)|`uniqueidentifier` |The base activity of the service activity. The activity contains the time frames, reminders, etc.|
|[Customer_Id](#customer_id)|`uniqueidentifier` |The receiver of the work|
|[Service_Agreement_Id](#service_agreement_id)|`uniqueidentifier` |The service agreement under which the work was done|
|[Location_Party_Contact_Mechanism_Id](#location_party_contact_mechanism_id)|`uniqueidentifier` |The location where or the communication line used to conduct the work|
|[Receiver_Person_Id](#receiver_person_id)|`uniqueidentifier` |The id of the person from the customers company, that received and signed for the service|
|[Receiver_Person_Name](#receiver_person_name)|`nvarchar(254)` |Copy of the name of the receiver at the time the activity was signed|
|[Store_Id](#store_id)|`uniqueidentifier` |The default store from which materials are taken|
|[Default_Service_Object_Id](#default_service_object_id)|`uniqueidentifier` |Default service object for materials and services lines|
|[Credit_Limit_Override](#credit_limit_override)|`bit` |Specifies a value, which would be provided to SalesOrder.CreditLimitOverride, when generating SalesOrder.|
|[Ship_To_Customer_Id](#ship_to_customer_id)|`uniqueidentifier` |Specific customer location of the main customer that receives the work.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Service_Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Agreement_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Location_Party_Contact_Mechanism_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiver_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Receiver_Person_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Service_Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Credit_Limit_Override

| Property | Value |
| - | - |
|Type|bit|

### Ship_To_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


