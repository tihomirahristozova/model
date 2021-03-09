# Table Crm_Sales_Order_Lines

Sales Orders detail records. Entity: Crm_Sales_Order_Lines

## Owner Tables Hierarchy

* [Crm_Sales_Orders](Crm_Sales_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive number of the line within the sales order|
|[Product_Id](#product_id)|`uniqueidentifier` |The product sold|
|[Product_Description](#product_description)|`nvarchar(254)` `ML`|The name of the sold product at the time the sale was made|
|[Requested_Quantity](#requested_quantity)|`decimal(12, 3)` |Quantity requested by customer|
|[Quantity](#quantity)|`decimal(12, 3)` |The quantity sold|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Quantity_Base](#quantity_base)|`decimal(12, 3)` |The equivalent of Quantity in the base measurement category of the product|
|[Unit_Price](#unit_price)|`decimal(14, 5)` |Unit price of the product in the currency of the sales order and in the unit of measure, as specified by QuantityUnitId|
|[Standard_Unit_Price](#standard_unit_price)|`decimal(14, 5)` Readonly|Standard unit price of the product during the creation of the sales order line|
|[Line_Amount](#line_amount)|`decimal(14, 2)` |The total amount for the line. Equals to Quantity * Unit_Price, less the discounts|
|[Line_Custom_Discount_Percent](#line_custom_discount_percent)|`decimal(7, 6)` |User-defined discount for the line|
|[Line_Discount_Id](#line_discount_id)|`uniqueidentifier` |The line discount type used to form the Line_Standard_Discount_Percent|
|[Line_Standard_Discount_Percent](#line_standard_discount_percent)|`decimal(7, 6)` Readonly|Standard discount for the line. This is automatically computed according to discount conditions|
|[Product_Price_Id](#product_price_id)|`uniqueidentifier` |Not NULL when the price has been selected from the list of valid standard prices|
|[Required_Delivery_Date](#required_delivery_date)|`date` |The required (contracted) delivery date for the line|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Guarantee period in days for the offered product. NULL for non-serviced products|
|[Bonus_Program_Id](#bonus_program_id)|`uniqueidentifier` |The bonus program, based on which the line was automatically added. NULL when the line was not added for bonus program.|
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |Used to set the Product_Id thru the coding systems|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Historical_Unit_Cost](#historical_unit_cost)|`decimal(14, 5)` |Used for returning of goods that are sold before the exploitation of the system|
|[Return_For_Sales_Order_Line_Id](#return_for_sales_order_line_id)|`uniqueidentifier` |When specified indicates that the goods sold in Return_For_Sales_Order_Line_Id are returned with the current line|
|[Line_Store_Id](#line_store_id)|`uniqueidentifier` |The store which should be used to issue the goods for the line. NULL means to use the store from the header|
|[Sales_Order_Line_Id](#sales_order_line_id)|`uniqueidentifier` `PK`||
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` ||
|[Line_Deal_Type_Id](#line_deal_type_id)|`uniqueidentifier` |Deal type to be passed to the invoice line. If deal type in entered then the invoice creates VAT entry for this deal type.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |Specifies the lot from which the goods should be issued. NULL means that the lot will be specified at a later stage (store order, etc.)|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Which serial number to receive/issue. NULL means that serial number is unknown or not applicable|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |The bin from which the goods should be withdrawn. NULL means that the bin will be specified at a later stage (store order, etc.)|
|[Promotional_Package_Id](#promotional_package_id)|`uniqueidentifier` Readonly|The promotional package, based on which the line was added. NULL when the line was not added as part of a promotional package|
|[Intrastat_Transport_Mode_Code](#intrastat_transport_mode_code)|`nvarchar(1)` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting|
|[Intrastat_Transport_Country_Id](#intrastat_transport_country_id)|`uniqueidentifier` |Country of origin of the transport company; used for Intrastat reporting|
|[Delivery_Terms_Code](#delivery_terms_code)|`nvarchar(3)` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting|
|[Intrastat_Transaction_Nature_Code](#intrastat_transaction_nature_code)|`nvarchar(2)` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting|
|[Persist_Lot](#persist_lot)|`bit` |If checked specifies that the lot in the line cannot be changed in the sub-documents created by the current document.|
|[Line_End_Customer_Party_Id](#line_end_customer_party_id)|`uniqueidentifier` |The end customer is the customer of the dealer. It is stored for information purposes only. The end customer may not have customer definition, just party.|
|[Historical_Data_Json](#historical_data_json)|`nvarchar(2147483647)` |Used only for lines, which are returns. It is a JSON-formatted string, containing data from the original sale.|
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(12, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|
|[Row_Version](#row_version)|`timestamp` ||
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute parent line.|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Line_From_Date](#line_from_date)|`date` |When selling a service valid only for a period, denotes the beginning of the period. NULL means that it is unknown or N/A.|
|[Return_For_Invoice_Line_Id](#return_for_invoice_line_id)|`uniqueidentifier` |When specified, indicates that the current line is a return for products, invoiced with the specified invoice line.|
|[Line_To_Date](#line_to_date)|`date` |When selling a service valid only for a period, denotes the end of the period. NULL means that it is unknown or N/A.|

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Requested_Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Unit_Price

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Standard_Unit_Price

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Line_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Line_Custom_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Line_Discount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Standard_Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Product_Price_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Delivery_Date

| Property | Value |
| - | - |
|Type|date|

### Guarantee_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Bonus_Program_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Historical_Unit_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Return_For_Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Promotional_Package_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Intrastat_Transport_Mode_Code

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Intrastat_Transport_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Delivery_Terms_Code

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Intrastat_Transaction_Nature_Code

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Persist_Lot

| Property | Value |
| - | - |
|Type|bit|

### Line_End_Customer_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Historical_Data_Json

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_From_Date

| Property | Value |
| - | - |
|Type|date|

### Return_For_Invoice_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_To_Date

| Property | Value |
| - | - |
|Type|date|


