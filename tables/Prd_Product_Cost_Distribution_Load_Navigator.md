# Query Prd_Product_Cost_Distribution_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Type](#type)|`nvarchar` ||
|[Transaction_Document_Type_Id](#transaction_document_type_id)|`uniqueidentifier` ||
|[Transaction_Document_Date](#transaction_document_date)|`date` ||
|[Transaction_Document_No](#transaction_document_no)|`nvarchar` ||
|[Transaction_Store_Id](#transaction_store_id)|`uniqueidentifier` ||
|[Transaction_Enterprise_Company_Id](#transaction_enterprise_company_id)|`uniqueidentifier` ||
|[Store_Transaction_Line_Id](#store_transaction_line_id)|`uniqueidentifier` `PK`||
|[Transaction_Line_No](#transaction_line_no)|`int` ||
|[Product_Id](#product_id)|`uniqueidentifier` |The item that was received/issued|
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` |The quantity of the stock received/issued in base measurement unit|
|[Adjusted_Base_Cost](#adjusted_base_cost)|`decimal(0, 0)` ||
|[Cost_Type_Id](#cost_type_id)|`uniqueidentifier` ||
|[Distributed_Amount_Base](#distributed_amount_base)|`decimal(0, 0)` |The amount (in base currency) of the distributed cost. The amount is calculated for the combination of output and cost type.|
|[Result_Line_No](#result_line_no)|`int` ||
|[Cost_Distribution_Id](#cost_distribution_id)|`uniqueidentifier` `PK`||
|[Start_Date](#start_date)|`date` ||
|[End_Date](#end_date)|`date` |The ending date of the covered period.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store (warehouse) for which the distribution is made. NULL means that the distribution covers multiple warehouses.|
|[Document_No](#document_no)|`nvarchar` |Document number, unique within Document_Type_Id|
|[Document_Date](#document_date)|`date` |The date on which the document was issued|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company which issued the document|

## Columns

### Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Transaction_Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Document_Date

| Property | Value |
| - | - |
|Type|date|

### Transaction_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Transaction_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Adjusted_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Cost_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Distributed_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Result_Line_No

| Property | Value |
| - | - |
|Type|int|

### Cost_Distribution_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Start_Date

| Property | Value |
| - | - |
|Type|date|

### End_Date

| Property | Value |
| - | - |
|Type|date|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


