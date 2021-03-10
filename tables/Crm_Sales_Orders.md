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


Customer_Id


The primary customer, which placed the sales order


The primary customer, which placed the sales order

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Customers](Crm_Customers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Customer_Id](Crm_Sales_Orders.md#customer_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Ship_To_Customer_Id


Ship_To_Customer_Id


The customer to whom to ship the sales order. Usually it is a customer entry for a sub-party of the primary customer


The customer to whom to ship the sales order. Usually it is a customer entry for a sub-party of the primary customer

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Customers](Crm_Customers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Ship_To_Customer_Id](Crm_Sales_Orders.md#ship_to_customer_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Price_List_Id


Price_List_Id


The price list to be used for determining product prices in the lines


The price list to be used for determining product prices in the lines

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Price_Lists](Crm_Price_Lists.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Price_List_Id](Crm_Sales_Orders.md#price_list_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Payment_Due_Date


Payment_Due_Date


The last term for the payment of the sales order


The last term for the payment of the sales order

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Payment_Due_Date](Crm_Sales_Orders.md#payment_due_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Payment_Type_Id


Payment_Type_Id


When not NULL specifies the payment type for the sales order


When not NULL specifies the payment type for the sales order

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cash_Payment_Types](Cash_Payment_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Payment_Type_Id](Crm_Sales_Orders.md#payment_type_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Required_Delivery_Date


Required_Delivery_Date


The required delivery date for all lines in the sales order. Initially calculated, based on either the Ship To Customer or Customer delivery term.


The required delivery date for all lines in the sales order. Initially calculated, based on either the Ship To Customer or Customer delivery term.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Required_Delivery_Date](Crm_Sales_Orders.md#required_delivery_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Store_Id


Store_Id


The store from which to issue the sales order. NULL means that there is no store associated with the sales order or there are different stores for some of the lines


The store from which to issue the sales order. NULL means that there is no store associated with the sales order or there are different stores for some of the lines

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Stores](Inv_Stores.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Store_Id](Crm_Sales_Orders.md#store_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|

### Intrastat_Transport_Country_Id


Intrastat_Transport_Country_Id


Country of origin of the transport company; used for Intrastat reporting


Country of origin of the transport company; used for Intrastat reporting

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Countries](Gen_Countries.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Intrastat_Transport_Country_Id](Crm_Sales_Orders.md#intrastat_transport_country_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Return_For_Invoice_Id


Return_For_Invoice_Id


When specified indicates that some of the goods sold in the sales orders invoiced with Return_For_Invoice_Id are returned with the current document


When specified indicates that some of the goods sold in the sales orders invoiced with Return_For_Invoice_Id are returned with the current document

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Invoices](Crm_Invoices.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Return_For_Invoice_Id](Crm_Sales_Orders.md#return_for_invoice_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Return_For_Sales_Order_Id


Return_For_Sales_Order_Id


When specified indicates that some of the goods sold in Return_For_Sales_Order_Id are returned with the current document


When specified indicates that some of the goods sold in Return_For_Sales_Order_Id are returned with the current document

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Sales_Orders](Crm_Sales_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Return_For_Sales_Order_Id](Crm_Sales_Orders.md#return_for_sales_order_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|yes|

### Customer_Purchase_Order_No


Customer_Purchase_Order_No


Reference number of the customer's purchase order


Reference number of the customer's purchase order

| Property | Value |
| - | - |
|Type|nvarchar(20)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Customer_Purchase_Order_No](Crm_Sales_Orders.md#customer_purchase_order_no)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|20|
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|Like|None|no|yes|

### Intrastat_Transaction_Nature_Code


Intrastat_Transaction_Nature_Code


Transaction nature; used for Intrastat reporting


Transaction nature; used for Intrastat reporting

| Property | Value |
| - | - |
|Type|nvarchar(2)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Intrastat_Transaction_Nature_Code](Crm_Sales_Orders.md#intrastat_transaction_nature_code)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2|
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Intrastat_Transport_Mode_Code


Intrastat_Transport_Mode_Code


Transport mode; used for Intrastat reporting


Transport mode; used for Intrastat reporting

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Intrastat_Transport_Mode_Code](Crm_Sales_Orders.md#intrastat_transport_mode_code)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|1|
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Delivery_Terms_Code


Delivery_Terms_Code


Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting


Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Delivery_Terms_Code](Crm_Sales_Orders.md#delivery_terms_code)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|3|
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Credit_Limit_Override


Credit_Limit_Override


Allows the sales order to be released even in the case of violations of credit limit or presence of overdue receivables


Allows the sales order to be released even in the case of violations of credit limit or presence of overdue receivables

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Credit_Limit_Override](Crm_Sales_Orders.md#credit_limit_override)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|14|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### IsValid


IsValid


1 when the order is valid (e.g. released and not void). Used for internal processing.


1 when the order is valid (e.g. released and not void). Used for internal processing.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[IsValid](Crm_Sales_Orders.md#isvalid)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|15|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Sales_Person_Id


Sales_Person_Id


Internal company sales person


Internal company sales person

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Sales_Persons](Crm_Sales_Persons.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Sales_Person_Id](Crm_Sales_Orders.md#sales_person_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|16|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Dealer_Id


Dealer_Id


The external dealer, associated with the sales order


The external dealer, associated with the sales order

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Dealers](Crm_Dealers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Dealer_Id](Crm_Sales_Orders.md#dealer_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|17|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Ship_To_Party_Contact_Mechanism_Id


Ship_To_Party_Contact_Mechanism_Id


The contact mechanism (address) to whih to ship the sales order


The contact mechanism (address) to whih to ship the sales order

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Party_Contact_Mechanisms](Cm_Party_Contact_Mechanisms.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Ship_To_Party_Contact_Mechanism_Id](Crm_Sales_Orders.md#ship_to_party_contact_mechanism_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|18|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Sales_Order_Id


Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Sales_Order_Id](Crm_Sales_Orders.md#sales_order_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|19|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Document_Id


Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Document_Id](Crm_Sales_Orders.md#document_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|20|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Document_Currency_Id


Document_Currency_Id


The currency of the document; e.g. the currency of the amounts in the document


The currency of the document; e.g. the currency of the amounts in the document

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Currencies](Gen_Currencies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Document_Currency_Id](Crm_Sales_Orders.md#document_currency_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|21|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Deal_Type_Id


Deal_Type_Id


Deal type to be passed to the invoice. If deal type in entered then the invoice creates VAT entry for this deal type.


Deal type to be passed to the invoice. If deal type in entered then the invoice creates VAT entry for this deal type.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[VAT_Deal_Types](VAT_Deal_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Deal_Type_Id](Crm_Sales_Orders.md#deal_type_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|22|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Notes](Crm_Sales_Orders.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|254|
|Order|23|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Deal_Id


Deal_Id


The opportunity (deal) on which this order is based


The opportunity (deal) on which this order is based

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Deals](Crm_Deals.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Deal_Id](Crm_Sales_Orders.md#deal_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|24|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Payment_Account_Id


Payment_Account_Id


When not NULL, the payment account, where the payment is expected. NULL=no expectation for account


When not NULL, the payment account, where the payment is expected. NULL=no expectation for account

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cash_Payment_Accounts](Cash_Payment_Accounts.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Payment_Account_Id](Crm_Sales_Orders.md#payment_account_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|25|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### End_Customer_Party_Id


End_Customer_Party_Id


The end customer is the customer of the dealer. It is stored for information purposes only. The end customer may not have customer definition; any party can be used.


The end customer is the customer of the dealer. It is stored for information purposes only. The end customer may not have customer definition; any party can be used.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Parties](Gen_Parties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[End_Customer_Party_Id](Crm_Sales_Orders.md#end_customer_party_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Fiscal_Sales_Number


Fiscal_Sales_Number


Unique number of the sale, assigned for fiscal reporting purposes. The format is according to the applicable legislation. NULL means that there is no requirement for fiscal sales number for this document or it is unknown.


Unique number of the sale, assigned for fiscal reporting purposes. The format is according to the applicable legislation. NULL means that there is no requirement for fiscal sales number for this document or it is unknown.

| Property | Value |
| - | - |
|Type|nvarchar(32)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Fiscal_Sales_Number](Crm_Sales_Orders.md#fiscal_sales_number)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|32|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Fiscal_Printer_Pos_Device_Id


Fiscal_Printer_Pos_Device_Id


For POS sales, specifies the fiscal printer. NULL when the sales is not a POS sale.


For POS sales, specifies the fiscal printer. NULL when the sales is not a POS sale.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Pos_Devices](Pos_Devices.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Fiscal_Printer_Pos_Device_Id](Crm_Sales_Orders.md#fiscal_printer_pos_device_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Pos_Operator_Id


Pos_Operator_Id


For POS sales, specifies the POS operator, who created the sale. NULL when the sale is not a POS sale.


For POS sales, specifies the POS operator, who created the sale. NULL when the sale is not a POS sale.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Pos_Operators](Pos_Operators.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Pos_Operator_Id](Crm_Sales_Orders.md#pos_operator_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Pos_Terminal_Id


Pos_Terminal_Id


For POS sales, specifies the POS terminal, on which the sale is entered. NULL when the sales is not a POS sale.


For POS sales, specifies the POS terminal, on which the sale is entered. NULL when the sales is not a POS sale.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Pos_Terminals](Pos_Terminals.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Pos_Terminal_Id](Crm_Sales_Orders.md#pos_terminal_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Pos_Location_Id


Pos_Location_Id


For POS sales, specifies the POS location, in which the sale is performed. NULL when the sales is not a POS sale.


For POS sales, specifies the POS location, in which the sale is performed. NULL when the sales is not a POS sale.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Pos_Locations](Pos_Locations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Pos_Location_Id](Crm_Sales_Orders.md#pos_location_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Is_Single_Execution


Is_Single_Execution


Specifies whether the document is a single execution of its order document.


Specifies whether the document is a single execution of its order document.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Is_Single_Execution](Crm_Sales_Orders.md#is_single_execution)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Is_Released


Is_Released


True if the document is not void and its state is released or greater


True if the document is not void and its state is released or greater

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Is_Released](Crm_Sales_Orders.md#is_released)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### From_Date


From_Date


When selling a service valid only for a period, denotes the beginning of the period. NULL means that it is unknown or N/A.


When selling a service valid only for a period, denotes the beginning of the period. NULL means that it is unknown or N/A.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[From_Date](Crm_Sales_Orders.md#from_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Payment_Due_Start_Date


Payment_Due_Start_Date


The date when the payment becomes due for documents with one installment. NULL when the document is with multiple installments.


The date when the payment becomes due for documents with one installment. NULL when the document is with multiple installments.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Payment_Due_Start_Date](Crm_Sales_Orders.md#payment_due_start_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Distribution_Channel_Id


Distribution_Channel_Id


The distribution channel, that is used to deliver the products


The distribution channel, that is used to deliver the products

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Distribution_Channels](Crm_Distribution_Channels.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Distribution_Channel_Id](Crm_Sales_Orders.md#distribution_channel_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Customer_Purchase_Order_Date


Customer_Purchase_Order_Date


Issue date of the referent customer purchase order


Issue date of the referent customer purchase order

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Customer_Purchase_Order_Date](Crm_Sales_Orders.md#customer_purchase_order_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|yes|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[Row_Version](Crm_Sales_Orders.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### To_Date


To_Date


When selling a service valid only for a period, denotes the end of the period. NULL means that it is unknown or N/A.


When selling a service valid only for a period, denotes the end of the period. NULL means that it is unknown or N/A.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders](Crm_Sales_Orders.md).[To_Date](Crm_Sales_Orders.md#to_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


