# Table Crm_Default_Sales_Order_Document_Properties

User-defined properties which shall be copied from the customer to the document for new documents of the specified document type. Entity: Crm_Default_Sales_Order_Document_Properties

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Default_Sales_Order_Document_Property_Id](#default_sales_order_document_property_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type for which the current definitions apply.|
|[Document_Property_Id](#document_property_id)|`uniqueidentifier` |The user-defined document property in which to copy the customers property value|
|[Customer_Property_Id](#customer_property_id)|`uniqueidentifier` |The user-defined customer property that shall be copied|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Default_Sales_Order_Document_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


