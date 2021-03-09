# Table Gen_Document_Fulfillments

Fulfillment ledger for documents. Entity: Gen_Document_Fulfillments (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Fulfillment_Id](#document_fulfillment_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The Document, which is fulfilled.|
|[Fulfillment_Type](#fulfillment_type)|`nvarchar(1)` Allowed: `P`, `C`|Type of fulfillment: P=Planned; C=Completed.|
|[Line_Type](#line_type)|`nvarchar(1)` |Detail (line) type, for example materials, services, etc. L=Line. Other values are defined by the document entity type.|
|[Document_Line_Id](#document_line_id)|`uniqueidentifier` |The Id of the fulfilled line within the document. The attribute contains the Id and is not a reference, because it references different entities depending on document entity type and line type.|
|[Line_No](#line_no)|`int` |Line number. Used for human-readability of the fulfillment. NULL if the lines do not support line numbers or the line number is unknown.|
|[Quantity_Base](#quantity_base)|`decimal(12, 3)` |Fulfilled quantity in the base measurement unit of the product.|
|[Is_Final](#is_final)|`bit` |Specifies whether this fulfillment finalizes the line, regardless of any remaining quantities.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` |The user, who created the record.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact time in UTC, when the fulfillment was created in the system.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Fulfillment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fulfillment_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Line_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Document_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Is_Final

| Property | Value |
| - | - |
|Type|bit|

### Creation_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Creation_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


