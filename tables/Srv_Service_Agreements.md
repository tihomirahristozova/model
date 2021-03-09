# Table Srv_Service_Agreements

Service agreements represent SLAs between the enterprise company and its clients. Entity: Srv_Service_Agreements

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Service_Agreement_Id](#service_agreement_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Customer_Id](#customer_id)|`uniqueidentifier` |The client of the service agreement.|
|[Start_Date_Time](#start_date_time)|`datetime` |Start date and time of the validity of the agreement.|
|[End_Date_Time](#end_date_time)|`datetime` |End date and time of the validity of the agreement.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Service_Agreement_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### End_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

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


