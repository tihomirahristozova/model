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

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Calendar_Date

| Property | Value |
| - | - |
|Type|datetime|

### Gross_Requirements

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Scheduled_Receipts

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Firm_Planned_Order_Receipts

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Firm_Planned_Order_Releases

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Planned_Order_Receipts

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Planned_Order_Releases

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Projected_Available_Balance

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Net_Requirements

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Explanation_Message

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Confirm_Action

| Property | Value |
| - | - |
|Type|bit|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Supplier_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Release_Date

| Property | Value |
| - | - |
|Type|datetime|

### Completion_Date

| Property | Value |
| - | - |
|Type|datetime|

### From_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Generation_Date

| Property | Value |
| - | - |
|Type|datetime|

### Requisition_Plan_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


