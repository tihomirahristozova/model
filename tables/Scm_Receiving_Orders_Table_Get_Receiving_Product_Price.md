# Procedure Scm_Receiving_Orders_Table_Get_Receiving_Product_Price


## Summary

| Name | Type | Description |
| - | - | --- |
|[Price_Per_Unit](#price_per_unit)|`decimal(14, 5)` |The unit price of the received products, in the documents currency.|
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` |The currency of the unit prices and amounts in the document.|

## Columns

### Price_Per_Unit


Price_Per_Unit


The unit price of the received products, in the documents currency.


The unit price of the received products, in the documents currency.

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
|Derived From|[Scm_Receiving_Order_Lines](Scm_Receiving_Order_Lines.md).[Price_Per_Unit](Scm_Receiving_Order_Lines.md#price_per_unit)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

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
|Derived From|[Scm_Receiving_Orders](Scm_Receiving_Orders.md).[Document_Currency_Id](Scm_Receiving_Orders.md#document_currency_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|


