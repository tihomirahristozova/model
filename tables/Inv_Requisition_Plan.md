# Table Inv_Requisition_Plan

The current requisition (MRP) plan. The data is deleted and re-created upon each planning. Entity: Inv_Requisition_Plan

## Summary

| Name | Type | Description |
| - | - | --- |
|[Store_Id](#store_id)|`uniqueidentifier` |The store, which is planned.|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, for which we are planning.|
|[Calendar_Date](#calendar_date)|`datetime` |The date for which we are planning. A record is created for each calendar date, on which there are events (orders, executions, planned events, etc.) for the product. Past events are stored on the current date of the planning.|
|[Gross_Requirements](#gross_requirements)|`decimal(18, 3)` |The gross requirements of the product on the specified calendar date. This is calculated as the unexecuted quantity of issue store orders, whose expected execution date is equal to the calendar date.|
|[Scheduled_Receipts](#scheduled_receipts)|`decimal(18, 3)` |The scheduled receipts of the product on the specified calendar date. This is calculated as the unexecuted quantity of released receipt store orders, whose expected execution date is equal to the calendar date.|
|[Firm_Planned_Order_Receipts](#firm_planned_order_receipts)|`decimal(18, 3)` |The quantity, which is expected to be received on the calendar date. The quantity is the same as the quantity, planned in Firm Planned Order Releases, but at a different calendar date - the expected receivement date.|
|[Firm_Planned_Order_Releases](#firm_planned_order_releases)|`decimal(18, 3)` |The order releases which were manually confirmed for release on the specified calendar date.|
|[Planned_Order_Receipts](#planned_order_receipts)|`decimal(18, 3)` |The planned by the calculation process order receipts on the calendar date. This is calculated by the MRP process as the quantity, which is expected to be received on the calendar date.|
|[Planned_Order_Releases](#planned_order_releases)|`decimal(18, 3)` |The planned by the calculation process order releases on the specified calendar date. This is calculated by the MRP process as the quantity, which should be released for purchasing, transfer or production on the calendar date.|
|[Projected_Available_Balance](#projected_available_balance)|`decimal(18, 3)` |Expected balance of the product for the calendar date. This is a calculation, based on the current physical inventory and expected future transactions.|
|[Net_Requirements](#net_requirements)|`decimal(18, 3)` |The net requirements for the date, which are in shortage for the calendar date.|
|[Explanation_Message](#explanation_message)|`nvarchar(2147483647)` |A message that explains why the program has generated the planned orders for this row|
|[Confirm_Action](#confirm_action)|`bit` |1 - generate firm planned orders for the current row; 0- do not generate;|
|[Quantity](#quantity)|`decimal(18, 3)` |The Quantity of the purchase orders the program shall generate; the suggested value equals Planned_Order_Releases but can be changed by the user;|
|[Supplier_Id](#supplier_id)|`uniqueidentifier` |The default supplier in the default product supply for current store, if any|
|[Release_Date](#release_date)|`datetime` |The suggested by the program value equals Calendar_Date; the release date of the purchase orders to be generated|
|[Completion_Date](#completion_date)|`datetime` |The suggested by the program value equals Calendar_Date + Planning_Lead_Time_Days of the default product supply for this store; the completion date of the purchase orders to be generated|
|[From_Store_Id](#from_store_id)|`uniqueidentifier` |When the order is for transfer, this is the store from which we shall transfer the product.|
|[Generation_Date](#generation_date)|`datetime` |Indicates the date on which the plan is generated|
|[Requisition_Plan_Item_Id](#requisition_plan_item_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Store_Id


Store_Id


The store, which is planned.


The store, which is planned.

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
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Store_Id](Inv_Requisition_Plan.md#store_id)|
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
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Product_Id


Product_Id


The product, for which we are planning.


The product, for which we are planning.

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
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Product_Id](Inv_Requisition_Plan.md#product_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Calendar_Date


Calendar_Date


The date for which we are planning. A record is created for each calendar date, on which there are events (orders, executions, planned events, etc.) for the product. Past events are stored on the current date of the planning.


The date for which we are planning. A record is created for each calendar date, on which there are events (orders, executions, planned events, etc.) for the product. Past events are stored on the current date of the planning.

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
|Default Value|None|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Calendar_Date](Inv_Requisition_Plan.md#calendar_date)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Gross_Requirements


Gross_Requirements


The gross requirements of the product on the specified calendar date. This is calculated as the unexecuted quantity of issue store orders, whose expected execution date is equal to the calendar date.


The gross requirements of the product on the specified calendar date. This is calculated as the unexecuted quantity of issue store orders, whose expected execution date is equal to the calendar date.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Gross_Requirements](Inv_Requisition_Plan.md#gross_requirements)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Scheduled_Receipts


Scheduled_Receipts


The scheduled receipts of the product on the specified calendar date. This is calculated as the unexecuted quantity of released receipt store orders, whose expected execution date is equal to the calendar date.


The scheduled receipts of the product on the specified calendar date. This is calculated as the unexecuted quantity of released receipt store orders, whose expected execution date is equal to the calendar date.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Scheduled_Receipts](Inv_Requisition_Plan.md#scheduled_receipts)|
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
|Supports EQUALS_IN|no|

### Firm_Planned_Order_Receipts


Firm_Planned_Order_Receipts


The quantity, which is expected to be received on the calendar date. The quantity is the same as the quantity, planned in Firm Planned Order Releases, but at a different calendar date - the expected receivement date.


The quantity, which is expected to be received on the calendar date. The quantity is the same as the quantity, planned in Firm Planned Order Releases, but at a different calendar date - the expected receivement date.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Firm_Planned_Order_Receipts](Inv_Requisition_Plan.md#firm_planned_order_receipts)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Firm_Planned_Order_Releases


Firm_Planned_Order_Releases


The order releases which were manually confirmed for release on the specified calendar date.


The order releases which were manually confirmed for release on the specified calendar date.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Firm_Planned_Order_Releases](Inv_Requisition_Plan.md#firm_planned_order_releases)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Planned_Order_Receipts


Planned_Order_Receipts


The planned by the calculation process order receipts on the calendar date. This is calculated by the MRP process as the quantity, which is expected to be received on the calendar date.


The planned by the calculation process order receipts on the calendar date. This is calculated by the MRP process as the quantity, which is expected to be received on the calendar date.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Planned_Order_Receipts](Inv_Requisition_Plan.md#planned_order_receipts)|
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
|Supports EQUALS_IN|no|

### Planned_Order_Releases


Planned_Order_Releases


The planned by the calculation process order releases on the specified calendar date. This is calculated by the MRP process as the quantity, which should be released for purchasing, transfer or production on the calendar date.


The planned by the calculation process order releases on the specified calendar date. This is calculated by the MRP process as the quantity, which should be released for purchasing, transfer or production on the calendar date.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Planned_Order_Releases](Inv_Requisition_Plan.md#planned_order_releases)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Projected_Available_Balance


Projected_Available_Balance


Expected balance of the product for the calendar date. This is a calculation, based on the current physical inventory and expected future transactions.


Expected balance of the product for the calendar date. This is a calculation, based on the current physical inventory and expected future transactions.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Projected_Available_Balance](Inv_Requisition_Plan.md#projected_available_balance)|
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
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Net_Requirements


Net_Requirements


The net requirements for the date, which are in shortage for the calendar date.


The net requirements for the date, which are in shortage for the calendar date.

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Net_Requirements](Inv_Requisition_Plan.md#net_requirements)|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Explanation_Message


Explanation_Message


A message that explains why the program has generated the planned orders for this row


A message that explains why the program has generated the planned orders for this row

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Explanation_Message](Inv_Requisition_Plan.md#explanation_message)|
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
|Max Length|2147483647|
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Confirm_Action


Confirm_Action


1 - generate firm planned orders for the current row; 0- do not generate;


1 - generate firm planned orders for the current row; 0- do not generate;

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
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Confirm_Action](Inv_Requisition_Plan.md#confirm_action)|
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
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Quantity


Quantity


The Quantity of the purchase orders the program shall generate; the suggested value equals Planned_Order_Releases but can be changed by the user;


The Quantity of the purchase orders the program shall generate; the suggested value equals Planned_Order_Releases but can be changed by the user;

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Quantity](Inv_Requisition_Plan.md#quantity)|
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
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Supplier_Id


Supplier_Id


The default supplier in the default product supply for current store, if any


The default supplier in the default product supply for current store, if any

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Scm_Suppliers](Scm_Suppliers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Supplier_Id](Inv_Requisition_Plan.md#supplier_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Release_Date


Release_Date


The suggested by the program value equals Calendar_Date; the release date of the purchase orders to be generated


The suggested by the program value equals Calendar_Date; the release date of the purchase orders to be generated

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
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Release_Date](Inv_Requisition_Plan.md#release_date)|
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
|Order|15|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Completion_Date


Completion_Date


The suggested by the program value equals Calendar_Date + Planning_Lead_Time_Days of the default product supply for this store; the completion date of the purchase orders to be generated


The suggested by the program value equals Calendar_Date + Planning_Lead_Time_Days of the default product supply for this store; the completion date of the purchase orders to be generated

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
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Completion_Date](Inv_Requisition_Plan.md#completion_date)|
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
|Supports EQUALS_IN|no|

### From_Store_Id


From_Store_Id


When the order is for transfer, this is the store from which we shall transfer the product.


When the order is for transfer, this is the store from which we shall transfer the product.

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
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[From_Store_Id](Inv_Requisition_Plan.md#from_store_id)|
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
|Order|17|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Generation_Date


Generation_Date


Indicates the date on which the plan is generated


Indicates the date on which the plan is generated

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
|Default Value|CurrentDateTime|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Generation_Date](Inv_Requisition_Plan.md#generation_date)|
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
|Order|17|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Requisition_Plan_Item_Id


Requisition_Plan_Item_Id

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
|Default Value|None|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Requisition_Plan_Item_Id](Inv_Requisition_Plan.md#requisition_plan_item_id)|
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

### Enterprise_Company_Id


Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Enterprise_Company_Id](Inv_Requisition_Plan.md#enterprise_company_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

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
|Derived From|[Inv_Requisition_Plan](Inv_Requisition_Plan.md).[Row_Version](Inv_Requisition_Plan.md#row_version)|
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


