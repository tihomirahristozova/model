# Table Inv_Cost_Corrections_Options

Options per document type for the cost corrections. Entity: Inv_Cost_Corrections_Options

## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Corrections_Option_Id](#cost_corrections_option_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type for which we specify the options.|
|[Reset_Transactions_State_On_Releasing](#reset_transactions_state_on_releasing)|`bit` |When true, the stock transactions state are re-set when the cost correction is released. The idea is to notify these documents, so that they have chance to re-generate their sub-documents.|
|[Schedule_Document_Events](#schedule_document_events)|`bit` |Indicates wheather the document events caused by the cost correction should be scheduled for later procession.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Cost_Corrections_Option_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reset_Transactions_State_On_Releasing

| Property | Value |
| - | - |
|Type|bit|

### Schedule_Document_Events

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


