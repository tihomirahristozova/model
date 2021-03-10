# Table Scm_Purchase_Invoice_Lines

Contains detail lines for purchase invoice documents. Entity: Scm_Purchase_Invoice_Lines

## Owner Tables Hierarchy

* [Scm_Purchase_Invoices](Scm_Purchase_Invoices.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchase_Invoice_Line_Id](#purchase_invoice_line_id)|`uniqueidentifier` `PK`||
|[Purchase_Invoice_Id](#purchase_invoice_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Consecutive line number within the invoice.|
|[Product_Id](#product_id)|`uniqueidentifier` |The invoiced product.|
|[Product_Name](#product_name)|`nvarchar(254)` `ML`|The name of the invoiced product, initially copied from the name in the product definition. The field can be edited by the user.|
|[Quantity](#quantity)|`decimal(12, 3)` |The invoiced quantity.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Unit_Price](#unit_price)|`decimal(14, 5)` |The unit price of the invoiced item in the document currency of the invoice.|
|[Line_Amount](#line_amount)|`decimal(14, 2)` |The total invoiced amount for this line in the document currency of the invoice.|
|[Line_Deal_Type_Id](#line_deal_type_id)|`uniqueidentifier` |Deal type for this line. If deal type in the line is different from deal type in the header another VAT entry is created.|
|[Line_Cost_Center_Id](#line_cost_center_id)|`uniqueidentifier` |Cost center for which the amount from this row will be accounted.|
|[Sale_Line_Deal_Type_Id](#sale_line_deal_type_id)|`uniqueidentifier` |Sale deal type for this line. If sale deal type in the line is different from sale deal type in the header another Sales VAT entry is created.|
|[Receiving_Order_Line_Id](#receiving_order_line_id)|`uniqueidentifier` |The receiving order line, which is invoiced by the current line. NULL means that this line is not directly related to receiving order line.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Quantity_Base](#quantity_base)|`decimal(12, 3)` |The equivalence of Quantity in the base measurement category of the product.|
|[Delivery_Terms_Code](#delivery_terms_code)|`nvarchar(3)` Allowed: `EXW`, `FCA`, `FAS`, `FOB`, `CFR`, `CIF`, `CPT`, `CIP`, `DAP`, `DAT`, `DDP`, `DPU`|Mode of delivery, like CIF, FOB, etc. Used also in Intrastat reporting|
|[Intrastat_Transaction_Nature_Code](#intrastat_transaction_nature_code)|`nvarchar(2)` Allowed: `11`, `12`, `13`, `14`, `19`, `21`, `22`, `23`, `29`, `60`, `70`, `80`, `91`, `99`, `30`, `41`, `42`, `51`, `52`|Transaction nature; used for Intrastat reporting|
|[Intrastat_Transport_Mode_Code](#intrastat_transport_mode_code)|`nvarchar(1)` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|Transport mode; used for Intrastat reporting|
|[Intrastat_Transport_Country_Id](#intrastat_transport_country_id)|`uniqueidentifier` |Country of origin of the transport company; used for Intrastat reporting|
|[Intrastat_Destination_Region_Id](#intrastat_destination_region_id)|`uniqueidentifier` |Region, which is the final destination of the goods. Used for Intrastat reporting.|
|[Origin_Country_Id](#origin_country_id)|`uniqueidentifier` |The country of origin of the invoiced product. Should be non-NULL only when this is different from the country of origin from the product definition.|
|[Intrastat_Apply_Date](#intrastat_apply_date)|`datetime` |Specifies in which period for Intrastat declaration must be included the current operation. Used only when the invoice is issued in different period than the one, that the operation must be included. If not set the document date is used.|
|[Row_Version](#row_version)|`timestamp` ||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(12, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

## Columns

### Purchase_Invoice_Line_Id


Purchase_Invoice_Line_Id

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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Purchase_Invoice_Line_Id](Scm_Purchase_Invoice_Lines.md#purchase_invoice_line_id)|
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

### Purchase_Invoice_Id


Purchase_Invoice_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Scm_Purchase_Invoices](Scm_Purchase_Invoices.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Purchase_Invoice_Id](Scm_Purchase_Invoice_Lines.md#purchase_invoice_id)|
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

### Line_No


Line_No


Consecutive line number within the invoice.


Consecutive line number within the invoice.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|10|
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Line_No](Scm_Purchase_Invoice_Lines.md#line_no)|
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
|Supports EQUALS_IN|no|

### Product_Id


Product_Id


The invoiced product.


The invoiced product.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Product_Id](Scm_Purchase_Invoice_Lines.md#product_id)|
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
|Equals|NULL|no|no|

### Product_Name


Product_Name


The name of the invoiced product, initially copied from the name in the product definition. The field can be edited by the user.


The name of the invoiced product, initially copied from the name in the product definition. The field can be edited by the user.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Product_Name](Scm_Purchase_Invoice_Lines.md#product_name)|
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
|Max Length|254|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Quantity


Quantity


The invoiced quantity.


The invoiced quantity.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Quantity](Scm_Purchase_Invoice_Lines.md#quantity)|
|Format|N3|
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
|Supports EQUALS_IN|no|

### Quantity_Unit_Id


Quantity_Unit_Id


The measurement unit of Quantity.


The measurement unit of Quantity.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Quantity_Unit_Id](Scm_Purchase_Invoice_Lines.md#quantity_unit_id)|
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
|Equals|NULL|no|no|

### Unit_Price


Unit_Price


The unit price of the invoiced item in the document currency of the invoice.


The unit price of the invoiced item in the document currency of the invoice.

| Property | Value |
| - | - |
|Type|decimal(14, 5)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Unit_Price](Scm_Purchase_Invoice_Lines.md#unit_price)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

### Line_Amount


Line_Amount


The total invoiced amount for this line in the document currency of the invoice.


The total invoiced amount for this line in the document currency of the invoice.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Line_Amount](Scm_Purchase_Invoice_Lines.md#line_amount)|
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
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Line_Deal_Type_Id


Line_Deal_Type_Id


Deal type for this line. If deal type in the line is different from deal type in the header another VAT entry is created.


Deal type for this line. If deal type in the line is different from deal type in the header another VAT entry is created.

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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Line_Deal_Type_Id](Scm_Purchase_Invoice_Lines.md#line_deal_type_id)|
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

### Line_Cost_Center_Id


Line_Cost_Center_Id


Cost center for which the amount from this row will be accounted.


Cost center for which the amount from this row will be accounted.

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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Line_Cost_Center_Id](Scm_Purchase_Invoice_Lines.md#line_cost_center_id)|
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

### Sale_Line_Deal_Type_Id


Sale_Line_Deal_Type_Id


Sale deal type for this line. If sale deal type in the line is different from sale deal type in the header another Sales VAT entry is created.


Sale deal type for this line. If sale deal type in the line is different from sale deal type in the header another Sales VAT entry is created.

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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Sale_Line_Deal_Type_Id](Scm_Purchase_Invoice_Lines.md#sale_line_deal_type_id)|
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
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Receiving_Order_Line_Id


Receiving_Order_Line_Id


The receiving order line, which is invoiced by the current line. NULL means that this line is not directly related to receiving order line.


The receiving order line, which is invoiced by the current line. NULL means that this line is not directly related to receiving order line.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Receiving_Order_Lines](Scm_Receiving_Order_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Receiving_Order_Line_Id](Scm_Purchase_Invoice_Lines.md#receiving_order_line_id)|
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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Notes](Scm_Purchase_Invoice_Lines.md#notes)|
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
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Quantity_Base


Quantity_Base


The equivalence of Quantity in the base measurement category of the product.


The equivalence of Quantity in the base measurement category of the product.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Quantity_Base](Scm_Purchase_Invoice_Lines.md#quantity_base)|
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
|Order|14|
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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Delivery_Terms_Code](Scm_Purchase_Invoice_Lines.md#delivery_terms_code)|
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
|Order|15|
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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Intrastat_Transaction_Nature_Code](Scm_Purchase_Invoice_Lines.md#intrastat_transaction_nature_code)|
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
|Order|16|
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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Intrastat_Transport_Mode_Code](Scm_Purchase_Invoice_Lines.md#intrastat_transport_mode_code)|
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
|Order|17|
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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Intrastat_Transport_Country_Id](Scm_Purchase_Invoice_Lines.md#intrastat_transport_country_id)|
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
|Order|18|
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


Region, which is the final destination of the goods. Used for Intrastat reporting.


Region, which is the final destination of the goods. Used for Intrastat reporting.

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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Intrastat_Destination_Region_Id](Scm_Purchase_Invoice_Lines.md#intrastat_destination_region_id)|
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

### Origin_Country_Id


Origin_Country_Id


The country of origin of the invoiced product. Should be non-NULL only when this is different from the country of origin from the product definition.


The country of origin of the invoiced product. Should be non-NULL only when this is different from the country of origin from the product definition.

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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Origin_Country_Id](Scm_Purchase_Invoice_Lines.md#origin_country_id)|
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

### Intrastat_Apply_Date


Intrastat_Apply_Date


Specifies in which period for Intrastat declaration must be included the current operation. Used only when the invoice is issued in different period than the one, that the operation must be included. If not set the document date is used.


Specifies in which period for Intrastat declaration must be included the current operation. Used only when the invoice is issued in different period than the one, that the operation must be included. If not set the document date is used.

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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Intrastat_Apply_Date](Scm_Purchase_Invoice_Lines.md#intrastat_apply_date)|
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
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Row_Version](Scm_Purchase_Invoice_Lines.md#row_version)|
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

### Standard_Quantity_Base


Standard_Quantity_Base


The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.


The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoice_Lines](Scm_Purchase_Invoice_Lines.md).[Standard_Quantity_Base](Scm_Purchase_Invoice_Lines.md#standard_quantity_base)|
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


