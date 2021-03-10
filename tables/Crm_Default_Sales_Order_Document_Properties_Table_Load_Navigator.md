# Query Crm_Default_Sales_Order_Document_Properties_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Default_Sales_Order_Document_Property_Id](#default_sales_order_document_property_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type for which the current definitions apply.|
|[Document_Property_Id](#document_property_id)|`uniqueidentifier` |The user-defined document property in which to copy the customers property value|
|[Customer_Property_Id](#customer_property_id)|`uniqueidentifier` |The user-defined customer property that shall be copied|

## Columns

### Default_Sales_Order_Document_Property_Id


Default_Sales_Order_Document_Property_Id

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
|Derived From|[Crm_Default_Sales_Order_Document_Properties](Crm_Default_Sales_Order_Document_Properties.md).[Default_Sales_Order_Document_Property_Id](Crm_Default_Sales_Order_Document_Properties.md#default_sales_order_document_property_id)|
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

### Document_Type_Id


Document_Type_Id


The document type for which the current definitions apply.


The document type for which the current definitions apply.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Default_Sales_Order_Document_Properties](Crm_Default_Sales_Order_Document_Properties.md).[Document_Type_Id](Crm_Default_Sales_Order_Document_Properties.md#document_type_id)|
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

### Document_Property_Id


Document_Property_Id


The user-defined document property in which to copy the customers property value


The user-defined document property in which to copy the customers property value

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Properties](Gen_Properties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Default_Sales_Order_Document_Properties](Crm_Default_Sales_Order_Document_Properties.md).[Document_Property_Id](Crm_Default_Sales_Order_Document_Properties.md#document_property_id)|
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

### Customer_Property_Id


Customer_Property_Id


The user-defined customer property that shall be copied


The user-defined customer property that shall be copied

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Properties](Gen_Properties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Default_Sales_Order_Document_Properties](Crm_Default_Sales_Order_Document_Properties.md).[Customer_Property_Id](Crm_Default_Sales_Order_Document_Properties.md#customer_property_id)|
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


