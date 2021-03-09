# Table Crm_Sales_Orders

Sales order document headers. Entity: Crm_Sales_Orders

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Customer_Id](#customer_id)|`uniqueidentifier` |The primary customer, which placed the sales order|
|[Ship_To_Customer_Id](#ship_to_customer_id)|`uniqueidentifier` |The customer to whom to ship the sales order. Usually it is a customer entry for a sub-party of the primary customer|
|[Price_List_Id](#price_list_id)|`uniqueidentifier` |The price list to be used for determining product prices in the lines|
|[Payment_Due_Date](#payment_due_date)|`datetime` |The last term for the payment of the sales order|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |When not NULL specifies the payment type for the sales order|
|[Required_Delivery_Date](#required_delivery_date)|`date` |The required delivery date for all lines in the sales order. Initially calculated, based on either the Ship To Customer or Customer delivery term.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store from which to issue the sales order. NULL means that there is no store associated with the sales order or there are different stores for some of the lines|
|[Intrastat_Transport_Country_Id](#intrastat_transport_country_id)|`uniqueidentifier` |Country of origin of the transport company; used for Intrastat reporting|
|[Return_For_Invoice_Id](#return_for_invoice_id)|`uniqueidentifier` |When specified indicates that some of the goods sold in the sales orders invoiced with Return_For_Invoice_Id are returned with the current document|
|[Return_For_Sales_Order_Id](#return_for_sales_order_id)|`uniqueidentifier` |When specified indicates that some of the goods sold in Return_For_Sales_Order_Id are returned with the current document|
|[Customer_Purchase_Order_No](#customer_purchase_order_no)|`nvarchar(20)` |Reference number of the customer's purchase order|
|[Intrastat_Transaction_Nature_Code](#intrastat_transaction_nature_code)|`nvarchar(2)` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting|
|[Intrastat_Transport_Mode_Code](#intrastat_transport_mode_code)|`nvarchar(1)` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting|
|[Delivery_Terms_Code](#delivery_terms_code)|`nvarchar(3)` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting|
|[Credit_Limit_Override](#credit_limit_override)|`bit` |Allows the sales order to be released even in the case of violations of credit limit or presence of overdue receivables|
|[IsValid](#isvalid)|`bit` |1 when the order is valid (e.g. released and not void). Used for internal processing.|
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` |Internal company sales person|
|[Dealer_Id](#dealer_id)|`uniqueidentifier` |The external dealer, associated with the sales order|
|[Ship_To_Party_Contact_Mechanism_Id](#ship_to_party_contact_mechanism_id)|`uniqueidentifier` |The contact mechanism (address) to whih to ship the sales order|
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency of the document; e.g. the currency of the amounts in the document|
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` |Deal type to be passed to the invoice. If deal type in entered then the invoice creates VAT entry for this deal type.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Deal_Id](#deal_id)|`uniqueidentifier` |The opportunity (deal) on which this order is based|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |When not NULL, the payment account, where the payment is expected. NULL=no expectation for account|
|[End_Customer_Party_Id](#end_customer_party_id)|`uniqueidentifier` |The end customer is the customer of the dealer. It is stored for information purposes only. The end customer may not have customer definition; any party can be used.|
|[Fiscal_Sales_Number](#fiscal_sales_number)|`nvarchar(32)` Readonly|Unique number of the sale, assigned for fiscal reporting purposes. The format is according to the applicable legislation. NULL means that there is no requirement for fiscal sales number for this document or it is unknown.|
|[Fiscal_Printer_Pos_Device_Id](#fiscal_printer_pos_device_id)|`uniqueidentifier` |For POS sales, specifies the fiscal printer. NULL when the sales is not a POS sale.|
|[Pos_Operator_Id](#pos_operator_id)|`uniqueidentifier` |For POS sales, specifies the POS operator, who created the sale. NULL when the sale is not a POS sale.|
|[Pos_Terminal_Id](#pos_terminal_id)|`uniqueidentifier` |For POS sales, specifies the POS terminal, on which the sale is entered. NULL when the sales is not a POS sale.|
|[Pos_Location_Id](#pos_location_id)|`uniqueidentifier` |For POS sales, specifies the POS location, in which the sale is performed. NULL when the sales is not a POS sale.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[From_Date](#from_date)|`date` |When selling a service valid only for a period, denotes the beginning of the period. NULL means that it is unknown or N/A.|
|[Payment_Due_Start_Date](#payment_due_start_date)|`datetime` |The date when the payment becomes due for documents with one installment. NULL when the document is with multiple installments.|
|[Distribution_Channel_Id](#distribution_channel_id)|`uniqueidentifier` |The distribution channel, that is used to deliver the products|
|[Customer_Purchase_Order_Date](#customer_purchase_order_date)|`date` |Issue date of the referent customer purchase order|
|[Row_Version](#row_version)|`timestamp` ||
|[To_Date](#to_date)|`date` |When selling a service valid only for a period, denotes the end of the period. NULL means that it is unknown or N/A.|

## Columns

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ship_To_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Due_Date

| Property | Value |
| - | - |
|Type|datetime|

### Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Delivery_Date

| Property | Value |
| - | - |
|Type|date|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Intrastat_Transport_Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Return_For_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Return_For_Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Purchase_Order_No

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Intrastat_Transaction_Nature_Code

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Intrastat_Transport_Mode_Code

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Delivery_Terms_Code

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Credit_Limit_Override

| Property | Value |
| - | - |
|Type|bit|

### IsValid

| Property | Value |
| - | - |
|Type|bit|

### Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Dealer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ship_To_Party_Contact_Mechanism_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Deal_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### End_Customer_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fiscal_Sales_Number

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Fiscal_Printer_Pos_Device_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Operator_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Terminal_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Location_Id

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

### From_Date

| Property | Value |
| - | - |
|Type|date|

### Payment_Due_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Distribution_Channel_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Purchase_Order_Date

| Property | Value |
| - | - |
|Type|date|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### To_Date

| Property | Value |
| - | - |
|Type|date|


