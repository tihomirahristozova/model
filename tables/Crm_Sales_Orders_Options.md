# Table Crm_Sales_Orders_Options

Options for sales orders of specific user defined document type. Entity: Crm_Sales_Orders_Options

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sales_Order_Option_Id](#sales_order_option_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type for which the sales order option applies.|
|[Available_Quantity_Only](#available_quantity_only)|`bit` |When 1 indicates that the sales order can be released only if there is sufficient available quantity (by ATP)|
|[Allowed_Directions](#allowed_directions)|`nvarchar(1)` Allowed: `S`, `R`, `*`, `A`|Allowed directions (return or normal sale) for the sales orders of this document type. 'S' = Normal sale, 'R' = Sales return, '*' = No limit, 'A' = Allow any, but not both (default)|
|[Minimum_Amount](#minimum_amount)|`decimal(14, 2)` |When not NULL, specifies minimal total amount of the sales order, which is required for order releasing.|
|[Minimum_Amount_Currency_Id](#minimum_amount_currency_id)|`uniqueidentifier` |The currency of Minimal Amount|
|[VAT_Deviation_Document_Amount_Type_Id](#vat_deviation_document_amount_type_id)|`uniqueidentifier` |Document amount that contains the difference between the total amount of the sales order formed by unit prices with VAT and the amount formed by unit prices without VAT|
|[Deal_Document_Type_Id](#deal_document_type_id)|`uniqueidentifier` |If filled then new opportunities (deals) from the specified type are created automatically by the sales orders that aren't assigned to existing opportunities.|
|[Shipment_Allowance](#shipment_allowance)|`nvarchar(1)` Allowed: `A`, `P`, `W`|Terms on which the shipment of the products in the sales order is allowed.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sales_Order_Option_Id


Sales_Order_Option_Id

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
|Derived From|[Crm_Sales_Orders_Options](Crm_Sales_Orders_Options.md).[Sales_Order_Option_Id](Crm_Sales_Orders_Options.md#sales_order_option_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Document_Type_Id


Document_Type_Id


The document type for which the sales order option applies.


The document type for which the sales order option applies.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders_Options](Crm_Sales_Orders_Options.md).[Document_Type_Id](Crm_Sales_Orders_Options.md#document_type_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Available_Quantity_Only


Available_Quantity_Only


When 1 indicates that the sales order can be released only if there is sufficient available quantity (by ATP)


When 1 indicates that the sales order can be released only if there is sufficient available quantity (by ATP)

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
|Derived From|[Crm_Sales_Orders_Options](Crm_Sales_Orders_Options.md).[Available_Quantity_Only](Crm_Sales_Orders_Options.md#available_quantity_only)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Allowed_Directions


Allowed_Directions


Allowed directions (return or normal sale) for the sales orders of this document type. 'S' = Normal sale, 'R' = Sales return, '*' = No limit, 'A' = Allow any, but not both (default)


Allowed directions (return or normal sale) for the sales orders of this document type. 'S' = Normal sale, 'R' = Sales return, '*' = No limit, 'A' = Allow any, but not both (default)

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`S`, `R`, `*`, `A`|
|Default Value|A|
|Derived From|[Crm_Sales_Orders_Options](Crm_Sales_Orders_Options.md).[Allowed_Directions](Crm_Sales_Orders_Options.md#allowed_directions)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Minimum_Amount


Minimum_Amount


When not NULL, specifies minimal total amount of the sales order, which is required for order releasing.


When not NULL, specifies minimal total amount of the sales order, which is required for order releasing.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders_Options](Crm_Sales_Orders_Options.md).[Minimum_Amount](Crm_Sales_Orders_Options.md#minimum_amount)|
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

### Minimum_Amount_Currency_Id


Minimum_Amount_Currency_Id


The currency of Minimal Amount


The currency of Minimal Amount

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Currencies](Gen_Currencies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders_Options](Crm_Sales_Orders_Options.md).[Minimum_Amount_Currency_Id](Crm_Sales_Orders_Options.md#minimum_amount_currency_id)|
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

### VAT_Deviation_Document_Amount_Type_Id


VAT_Deviation_Document_Amount_Type_Id


Document amount that contains the difference between the total amount of the sales order formed by unit prices with VAT and the amount formed by unit prices without VAT


Document amount that contains the difference between the total amount of the sales order formed by unit prices with VAT and the amount formed by unit prices without VAT

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders_Options](Crm_Sales_Orders_Options.md).[VAT_Deviation_Document_Amount_Type_Id](Crm_Sales_Orders_Options.md#vat_deviation_document_amount_type_id)|
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

### Deal_Document_Type_Id


Deal_Document_Type_Id


If filled then new opportunities (deals) from the specified type are created automatically by the sales orders that aren't assigned to existing opportunities.


If filled then new opportunities (deals) from the specified type are created automatically by the sales orders that aren't assigned to existing opportunities.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Orders_Options](Crm_Sales_Orders_Options.md).[Deal_Document_Type_Id](Crm_Sales_Orders_Options.md#deal_document_type_id)|
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

### Shipment_Allowance


Shipment_Allowance


Terms on which the shipment of the products in the sales order is allowed.


Terms on which the shipment of the products in the sales order is allowed.

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`A`, `P`, `W`|
|Default Value|A|
|Derived From|[Crm_Sales_Orders_Options](Crm_Sales_Orders_Options.md).[Shipment_Allowance](Crm_Sales_Orders_Options.md#shipment_allowance)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

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
|Derived From|[Crm_Sales_Orders_Options](Crm_Sales_Orders_Options.md).[Row_Version](Crm_Sales_Orders_Options.md#row_version)|
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


