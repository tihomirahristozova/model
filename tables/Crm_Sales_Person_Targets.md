# Table Crm_Sales_Person_Targets

Sales person targets document header. Targets are expressed in amount or other numeric objectives and are tracked in achieved percentages. Entity: Crm_Sales_Person_Targets

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sales_Person_Target_Id](#sales_person_target_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` |Sales person to whom the target is assigned. Serves as default for the lines.|
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` |Product group for which the target is defined. Serves as default for the lines.|
|[Target_Currency_Id](#target_currency_id)|`uniqueidentifier` |Denotes the currency of amount targets. Required when amount targets are present in the documnet.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sales_Person_Target_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Target_Currency_Id

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


