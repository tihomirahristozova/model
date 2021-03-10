# View Inv_Store_Order_Lines_Unfulfilled_View

Returns the remaining (unfulfilled) quantity and cost for each Store Order Line in Store Orders, which are Planned, FirmPlanned or Released. Is_Fulfilled and Is_QuantityFulfilled can be used to filter out lines which appear fulfilled. For best performance, the store orders should be finished after fulfilling. Entity: Inv_Store_Order_Lines_Unfulfilled_View (Introduced in version 21.1.1.16)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Which serial number to receive/issue. NULL means that serial number is unknown or not applicable|
|[Lot_Id](#lot_id)|`uniqueidentifier` |If non-null, contains the specific lot to use for the movement|
|[Store_Order_Line_Id](#store_order_line_id)|`uniqueidentifier` ||
|[Document_Date](#document_date)|`datetime` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Order_Remaining_Quantity_Base](#order_remaining_quantity_base)|`decimal(38, 3)` |The remaining (unfulfilled) quantity of the order line in base measurement unit.|
|[Order_Remaining_Line_Cost](#order_remaining_line_cost)|`decimal(38, 2)` |The remaining (unfulfilled) line cost of the order line.|
|[Is_Fulfilled](#is_fulfilled)|`int` |Returns 1/true when both the Quantity and Cost are fulfilled or only negligible (less than 0.001 for qty and 0.01 for cost) sums remain. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling.|
|[Is_QuantityFulfilled](#is_quantityfulfilled)|`int` |Returns 1/true when the Quantity is fulfilled or only negligible (less than 0.001) sum remains. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling.|

## Columns

### Serial_Number_Id


Serial_Number_Id


Which serial number to receive/issue. NULL means that serial number is unknown or not applicable


Which serial number to receive/issue. NULL means that serial number is unknown or not applicable

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Serial_Numbers](Inv_Serial_Numbers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Store_Order_Lines](Inv_Store_Order_Lines.md).[Serial_Number_Id](Inv_Store_Order_Lines.md#serial_number_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|

### Lot_Id


Lot_Id


If non-null, contains the specific lot to use for the movement


If non-null, contains the specific lot to use for the movement

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Lots](Inv_Lots.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Store_Order_Lines](Inv_Store_Order_Lines.md).[Lot_Id](Inv_Store_Order_Lines.md#lot_id)|
|Depends On|[Product_Id](#product_id)|
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
|Order|17|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Store_Order_Line_Id


Store_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Inv_Store_Order_Lines](Inv_Store_Order_Lines.md).[Store_Order_Line_Id](Inv_Store_Order_Lines.md#store_order_line_id)|
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

### Document_Date


Document_Date

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDate|
|Derived From|[Gen_Documents](Gen_Documents.md).[Document_Date](Gen_Documents.md#document_date)|
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
|Equals|NULL|no|yes|
|GreaterThanOrLessThan|None|yes|no|

### Enterprise_Company_Id


Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Documents](Gen_Documents.md).[Enterprise_Company_Id](Gen_Documents.md#enterprise_company_id)|
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

### Store_Id


Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Stores](Inv_Stores.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Store_Orders](Inv_Store_Orders.md).[Store_Id](Inv_Store_Orders.md#store_id)|
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

### Product_Id


Product_Id

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
|Derived From|[Inv_Store_Order_Lines](Inv_Store_Order_Lines.md).[Product_Id](Inv_Store_Order_Lines.md#product_id)|
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

### Product_Variant_Id


Product_Variant_Id


If specified determines which product variant of the current product in this line is used.


If specified determines which product variant of the current product in this line is used.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Product_Variants](Gen_Product_Variants.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Store_Order_Lines](Inv_Store_Order_Lines.md).[Product_Variant_Id](Inv_Store_Order_Lines.md#product_variant_id)|
|Depends On|[Product_Id](#product_id)|
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
|Equals|NULL|yes|yes|

### Order_Remaining_Quantity_Base


Order_Remaining_Quantity_Base


The remaining (unfulfilled) quantity of the order line in base measurement unit.


The remaining (unfulfilled) quantity of the order line in base measurement unit.

| Property | Value |
| - | - |
|Type|decimal(38, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Store_Order_Lines_Unfulfilled_View](Inv_Store_Order_Lines_Unfulfilled_View.md).[Order_Remaining_Quantity_Base](Inv_Store_Order_Lines_Unfulfilled_View.md#order_remaining_quantity_base)|
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
|Equals|NULL|no|yes|
|GreaterThanOrLessThan|None|no|no|

### Order_Remaining_Line_Cost


Order_Remaining_Line_Cost


The remaining (unfulfilled) line cost of the order line.


The remaining (unfulfilled) line cost of the order line.

| Property | Value |
| - | - |
|Type|decimal(38, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Store_Order_Lines_Unfulfilled_View](Inv_Store_Order_Lines_Unfulfilled_View.md).[Order_Remaining_Line_Cost](Inv_Store_Order_Lines_Unfulfilled_View.md#order_remaining_line_cost)|
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
|Equals|NULL|no|yes|
|GreaterThanOrLessThan|None|no|no|

### Is_Fulfilled


Is_Fulfilled


Returns 1/true when both the Quantity and Cost are fulfilled or only negligible (less than 0.001 for qty and 0.01 for cost) sums remain. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling.


Returns 1/true when both the Quantity and Cost are fulfilled or only negligible (less than 0.001 for qty and 0.01 for cost) sums remain. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling.

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
|Derived From|[Inv_Store_Order_Lines_Unfulfilled_View](Inv_Store_Order_Lines_Unfulfilled_View.md).[Is_Fulfilled](Inv_Store_Order_Lines_Unfulfilled_View.md#is_fulfilled)|
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
|Equals|NULL|no|yes|

### Is_QuantityFulfilled


Is_QuantityFulfilled


Returns 1/true when the Quantity is fulfilled or only negligible (less than 0.001) sum remains. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling.


Returns 1/true when the Quantity is fulfilled or only negligible (less than 0.001) sum remains. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling.

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
|Derived From|[Inv_Store_Order_Lines_Unfulfilled_View](Inv_Store_Order_Lines_Unfulfilled_View.md).[Is_QuantityFulfilled](Inv_Store_Order_Lines_Unfulfilled_View.md#is_quantityfulfilled)|
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
|Equals|NULL|no|yes|


