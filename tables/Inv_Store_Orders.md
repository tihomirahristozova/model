# Table Inv_Store_Orders

Orders for store transactions. After an order is executed, store transaction is created. Entity: Inv_Store_Orders

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Store_Order_Id](#store_order_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The Id of the store order document entry|
|[Store_Id](#store_id)|`uniqueidentifier` |The designated warehouse for the operation|
|[Due_Date](#due_date)|`datetime` |The final date, when the store transaction should occur.|
|[Movement_Type](#movement_type)|`nvarchar(1)` Allowed: `I`, `R`|Store order movement type. R=RECEIPT, I=ISSUE|
|[Status](#status)|`nvarchar(1)` |P=Planned; F=Firm planned; R=Released; C=Completed|
|[Planned_Release_Date](#planned_release_date)|`datetime` |Date, when the respective store transaction document is scheduled to be released to the supplier or manufacturing. This is respected by all PAB (projected available balance) and ATP (available to promise) calculations as the date on which the store transaction is scheduled to occur.|
|[Planned_Completion_Date](#planned_completion_date)|`datetime` |Date, when the quantities are expected to be completely issued/received|
|[Driver_Name](#driver_name)|`nvarchar(64)` |The name of the driver, who will deliver the stocks.|
|[Temp_Transport_Company_Name](#temp_transport_company_name)|`nvarchar(64)` |Obsolete. Not used.|
|[Vehicle_Reg_Number](#vehicle_reg_number)|`nvarchar(32)` |Obsolete. Not used.|
|[Ordering_Person_Id](#ordering_person_id)|`uniqueidentifier` |The person, which ordered the operation.|
|[Issued_By_Party_Id](#issued_by_party_id)|`uniqueidentifier` |The party, which issued the goods.|
|[Received_By_Party_Id](#received_by_party_id)|`uniqueidentifier` |The party, which received the goods.|
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency in which the document amounts are expessed.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

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

### Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Movement_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Status

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Planned_Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Planned_Completion_Date

| Property | Value |
| - | - |
|Type|datetime|

### Driver_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Temp_Transport_Company_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Vehicle_Reg_Number

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Ordering_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Issued_By_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Received_By_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


