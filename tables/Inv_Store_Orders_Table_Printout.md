# Procedure Inv_Store_Orders_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Store_Order_Id](#store_order_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The Id of the store order document entry|
|[Store_Id](#store_id)|`uniqueidentifier` |The designated warehouse for the operation|
|[Store_Name](#store_name)|`nvarchar` ||
|[Due_Date](#due_date)|`datetime` |The final date, when the store transaction should occur.|
|[Movement_Type](#movement_type)|`nvarchar` Allowed: `I`, `R`|Store order movement type. R=RECEIPT, I=ISSUE|
|[Status](#status)|`nvarchar` |P=Planned; F=Firm planned; R=Released; C=Completed|
|[Planned_Release_Date](#planned_release_date)|`datetime` |Date, when the respective store transaction document is scheduled to be released to the supplier or manufacturing. This is respected by all PAB (projected available balance) and ATP (available to promise) calculations as the date on which the store transaction is scheduled to occur.|
|[Planned_Completion_Date](#planned_completion_date)|`datetime` |Date, when the quantities are expected to be completely issued/received|
|[Responsible_Party_Name](#responsible_party_name)|`nvarchar` ||
|[Driver_Name](#driver_name)|`nvarchar` ||
|[Temp_Transport_Company_Name](#temp_transport_company_name)|`nvarchar` ||
|[Vehicle_Reg_Number](#vehicle_reg_number)|`nvarchar` |Obsolete. Not used.|
|[Ordering_Person_Id](#ordering_person_id)|`uniqueidentifier` |The person, which ordered the operation.|
|[Ordering_Person_Name](#ordering_person_name)|`nvarchar` ||
|[Issued_By_Party_Id](#issued_by_party_id)|`uniqueidentifier` |The party, which issued the goods.|
|[Issued_By_Party_Name](#issued_by_party_name)|`nvarchar` ||
|[Received_By_Party_Id](#received_by_party_id)|`uniqueidentifier` |The party, which received the goods.|
|[Received_By_Party_Name](#received_by_party_name)|`nvarchar` ||

## Columns

### Store_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Movement_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Status

| Property | Value |
| - | - |
|Type|nvarchar|

### Planned_Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Planned_Completion_Date

| Property | Value |
| - | - |
|Type|datetime|

### Responsible_Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Driver_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Temp_Transport_Company_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Vehicle_Reg_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Ordering_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ordering_Person_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Issued_By_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Issued_By_Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Received_By_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Received_By_Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|


