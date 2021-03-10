# Table Scm_Purchase_Invoices

Contains purchase invoice headers. Entity: Scm_Purchase_Invoices

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Invoice_Id](#purchase_invoice_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Supplier_Id](#supplier_id)|`uniqueidentifier` |The supplier of the purchase, who is issuing the document.|
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency of the unit prices and amounts in the document.|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |The payment type to be used. NULL is allowed only temporary and should be specified if payment order is to be generated|
|[Purchase_Order_Id](#purchase_order_id)|`uniqueidentifier` |The purchase order that was sent to the supplier and is the base for the invoice. NULL means there is no linked PO and 3 way check won't be performed|
|[Receiving_Order_Id](#receiving_order_id)|`uniqueidentifier` |The receiving order for the goods that were invoiced. The id is used for 2 or 3 way quantity check. NULL means that there is no linked RO and the 2 or 3 way check will not include the RO|
|[Credit_Note_Original_Purchase_Invoice_Id](#credit_note_original_purchase_invoice_id)|`uniqueidentifier` |The original invoice, which is debited/credited with this note|
|[Credit_Note_Reason](#credit_note_reason)|`nvarchar(254)` |Reason for the debit/credit note|
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` |Deal type for this purchase invoice. If deal type in entered then VAT entry is created for this deal type.|
|[Cost_Center_Id](#cost_center_id)|`uniqueidentifier` |Cost center for which the amount from this document will be accounted.|
|[Apply_Date](#apply_date)|`date` |Specifies the date on which to create the VAT ledger entry for this purchase invoice. Usually, this date is equal to the document date, except when the document is received too late to be applied on its original document date.|
|[Sale_Deal_Type_Id](#sale_deal_type_id)|`uniqueidentifier` |Sale deal type for this purchase invoice. If sale deal type in entered then Sales VAT entry is created for this deal type.|
|[VAT_Notes](#vat_notes)|`nvarchar(254)` |Description of the operation that will be entered in the VAT ledgers.|
|[Payment_Due_Date](#payment_due_date)|`datetime` |Due date for paying the invoice. NULL means to use the default |
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |When not NULL, specifies the default payment account for the payment order|
|[Purchase_Price_List_Id](#purchase_price_list_id)|`uniqueidentifier` |The price list, which, when non-NULL, is used to automatically load unit prices of the products, when entering the invoice manually.|
|[Delivery_Terms_Code](#delivery_terms_code)|`nvarchar(3)` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting|
|[Intrastat_Transaction_Nature_Code](#intrastat_transaction_nature_code)|`nvarchar(2)` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting|
|[Intrastat_Transport_Mode_Code](#intrastat_transport_mode_code)|`nvarchar(1)` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting|
|[Intrastat_Transport_Country_Id](#intrastat_transport_country_id)|`uniqueidentifier` |Country of origin of the transport company; used for Intrastat reporting|
|[Intrastat_Destination_Region_Id](#intrastat_destination_region_id)|`uniqueidentifier` |Region, which is the final destination of the goods. Used for Intrastat reporting. When this is non-NULL, it applies to the whole document.|
|[VAT_Cash_Reporting_Mode](#vat_cash_reporting_mode)|`bit` |When True, indicates, that this invoice uses the special 'Cash reporting mode' when creating VAT ledger entries.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Purchase_Invoice_Id


Purchase_Invoice_Id

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Purchase_Invoice_Id](Scm_Purchase_Invoices.md#purchase_invoice_id)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Document_Id](Scm_Purchase_Invoices.md#document_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Supplier_Id


Supplier_Id


The supplier of the purchase, who is issuing the document.


The supplier of the purchase, who is issuing the document.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Suppliers](Scm_Suppliers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Supplier_Id](Scm_Purchase_Invoices.md#supplier_id)|
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
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Document_Currency_Id


Document_Currency_Id


The currency of the unit prices and amounts in the document.


The currency of the unit prices and amounts in the document.

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Document_Currency_Id](Scm_Purchase_Invoices.md#document_currency_id)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Payment_Type_Id


Payment_Type_Id


The payment type to be used. NULL is allowed only temporary and should be specified if payment order is to be generated


The payment type to be used. NULL is allowed only temporary and should be specified if payment order is to be generated

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Payment_Type_Id](Scm_Purchase_Invoices.md#payment_type_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Purchase_Order_Id


Purchase_Order_Id


The purchase order that was sent to the supplier and is the base for the invoice. NULL means there is no linked PO and 3 way check won't be performed


The purchase order that was sent to the supplier and is the base for the invoice. NULL means there is no linked PO and 3 way check won't be performed

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Purchase_Orders](Scm_Purchase_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Purchase_Order_Id](Scm_Purchase_Invoices.md#purchase_order_id)|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Receiving_Order_Id


Receiving_Order_Id


The receiving order for the goods that were invoiced. The id is used for 2 or 3 way quantity check. NULL means that there is no linked RO and the 2 or 3 way check will not include the RO


The receiving order for the goods that were invoiced. The id is used for 2 or 3 way quantity check. NULL means that there is no linked RO and the 2 or 3 way check will not include the RO

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Receiving_Orders](Scm_Receiving_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Receiving_Order_Id](Scm_Purchase_Invoices.md#receiving_order_id)|
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
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Credit_Note_Original_Purchase_Invoice_Id


Credit_Note_Original_Purchase_Invoice_Id


The original invoice, which is debited/credited with this note


The original invoice, which is debited/credited with this note

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Credit_Note_Original_Purchase_Invoice_Id](Scm_Purchase_Invoices.md#credit_note_original_purchase_invoice_id)|
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
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Credit_Note_Reason


Credit_Note_Reason


Reason for the debit/credit note


Reason for the debit/credit note

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Credit_Note_Reason](Scm_Purchase_Invoices.md#credit_note_reason)|
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
|Max Length|254|
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Deal_Type_Id


Deal_Type_Id


Deal type for this purchase invoice. If deal type in entered then VAT entry is created for this deal type.


Deal type for this purchase invoice. If deal type in entered then VAT entry is created for this deal type.

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Deal_Type_Id](Scm_Purchase_Invoices.md#deal_type_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Cost_Center_Id


Cost_Center_Id


Cost center for which the amount from this document will be accounted.


Cost center for which the amount from this document will be accounted.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Acc_Cost_Centers](Acc_Cost_Centers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Cost_Center_Id](Scm_Purchase_Invoices.md#cost_center_id)|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Apply_Date


Apply_Date


Specifies the date on which to create the VAT ledger entry for this purchase invoice. Usually, this date is equal to the document date, except when the document is received too late to be applied on its original document date.


Specifies the date on which to create the VAT ledger entry for this purchase invoice. Usually, this date is equal to the document date, except when the document is received too late to be applied on its original document date.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Apply_Date](Scm_Purchase_Invoices.md#apply_date)|
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
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Sale_Deal_Type_Id


Sale_Deal_Type_Id


Sale deal type for this purchase invoice. If sale deal type in entered then Sales VAT entry is created for this deal type.


Sale deal type for this purchase invoice. If sale deal type in entered then Sales VAT entry is created for this deal type.

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Sale_Deal_Type_Id](Scm_Purchase_Invoices.md#sale_deal_type_id)|
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
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### VAT_Notes


VAT_Notes


Description of the operation that will be entered in the VAT ledgers.


Description of the operation that will be entered in the VAT ledgers.

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[VAT_Notes](Scm_Purchase_Invoices.md#vat_notes)|
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
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Payment_Due_Date


Payment_Due_Date


Due date for paying the invoice. NULL means to use the default 


Due date for paying the invoice. NULL means to use the default 

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Payment_Due_Date](Scm_Purchase_Invoices.md#payment_due_date)|
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
|Order|14|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Payment_Account_Id


Payment_Account_Id


When not NULL, specifies the default payment account for the payment order


When not NULL, specifies the default payment account for the payment order

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Payment_Account_Id](Scm_Purchase_Invoices.md#payment_account_id)|
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
|Order|15|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Purchase_Price_List_Id


Purchase_Price_List_Id


The price list, which, when non-NULL, is used to automatically load unit prices of the products, when entering the invoice manually.


The price list, which, when non-NULL, is used to automatically load unit prices of the products, when entering the invoice manually.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Purchase_Price_Lists](Scm_Purchase_Price_Lists.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Purchase_Price_List_Id](Scm_Purchase_Invoices.md#purchase_price_list_id)|
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
|Order|16|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Delivery_Terms_Code](Scm_Purchase_Invoices.md#delivery_terms_code)|
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
|Order|17|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Intrastat_Transaction_Nature_Code](Scm_Purchase_Invoices.md#intrastat_transaction_nature_code)|
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
|Order|18|
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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Intrastat_Transport_Mode_Code](Scm_Purchase_Invoices.md#intrastat_transport_mode_code)|
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
|Order|19|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Intrastat_Transport_Country_Id](Scm_Purchase_Invoices.md#intrastat_transport_country_id)|
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
|Order|20|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Intrastat_Destination_Region_Id


Intrastat_Destination_Region_Id


Region, which is the final destination of the goods. Used for Intrastat reporting. When this is non-NULL, it applies to the whole document.


Region, which is the final destination of the goods. Used for Intrastat reporting. When this is non-NULL, it applies to the whole document.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Administrative_Regions](Gen_Administrative_Regions.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Intrastat_Destination_Region_Id](Scm_Purchase_Invoices.md#intrastat_destination_region_id)|
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

### VAT_Cash_Reporting_Mode


VAT_Cash_Reporting_Mode


When True, indicates, that this invoice uses the special 'Cash reporting mode' when creating VAT ledger entries.


When True, indicates, that this invoice uses the special 'Cash reporting mode' when creating VAT ledger entries.

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[VAT_Cash_Reporting_Mode](Scm_Purchase_Invoices.md#vat_cash_reporting_mode)|
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
|Equals|NULL|no|no|

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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Is_Single_Execution](Scm_Purchase_Invoices.md#is_single_execution)|
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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Is_Released](Scm_Purchase_Invoices.md#is_released)|
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
|Derived From|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md).[Row_Version](Scm_Purchase_Invoices.md#row_version)|
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


