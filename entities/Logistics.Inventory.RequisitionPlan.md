---
uid: Logistics.Inventory.RequisitionPlan
---
# Logistics.Inventory.RequisitionPlan

The current requisition (MRP) plan. The data is deleted and re-created upon each planning. Entity: Inv_Requisition_Plan

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CalendarDate](Logistics.Inventory.RequisitionPlan.md#calendardate) | datetime | The date for which we are planning. A record is created for each calendar date, on which there are events (orders, executions, planned events, etc.) for the product. Past events are stored on the current date of the planning. [Required] [Filter(ge;le)] 
| [CompletionDate](Logistics.Inventory.RequisitionPlan.md#completiondate) | datetime (nullable) | The suggested by the program value equals Calendar_Date + Planning_Lead_Time_Days of the default product supply for this store; the completion date of the purchase orders to be generated. 
| [ConfirmAction](Logistics.Inventory.RequisitionPlan.md#confirmaction) | boolean | True - generate firm planned orders for the current row; false- do not generate;. [Required] [Default(false)] [Filter(eq)] 
| [ExplanationMessage](Logistics.Inventory.RequisitionPlan.md#explanationmessage) | string (nullable) | A message that explains why the program has generated the planned orders for this row. 
| [FirmPlannedOrderReceipts](Logistics.Inventory.RequisitionPlan.md#firmplannedorderreceipts) | [Quantity](../data-types.md#quantity) | The quantity, which is expected to be received on the calendar date. The quantity is the same as the quantity, planned in Firm Planned Order Releases, but at a different calendar date - the expected receivement date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 
| [FirmPlannedOrderReleases](Logistics.Inventory.RequisitionPlan.md#firmplannedorderreleases) | [Quantity](../data-types.md#quantity) | The order releases which were manually confirmed for release on the specified calendar date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 
| [GenerationDate](Logistics.Inventory.RequisitionPlan.md#generationdate) | datetime | Indicates the date on which the plan is generated. [Required] [Default(Now)] 
| [GrossRequirements](Logistics.Inventory.RequisitionPlan.md#grossrequirements) | [Quantity](../data-types.md#quantity) | The gross requirements of the product on the specified calendar date. This is calculated as the unexecuted quantity of issue store orders, whose expected execution date is equal to the calendar date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 
| [Id](Logistics.Inventory.RequisitionPlan.md#id) | guid |  
| [NetRequirements](Logistics.Inventory.RequisitionPlan.md#netrequirements) | [Quantity](../data-types.md#quantity) | The net requirements for the date, which are in shortage for the calendar date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 
| [PlannedOrderReceipts](Logistics.Inventory.RequisitionPlan.md#plannedorderreceipts) | [Quantity](../data-types.md#quantity) | The planned by the calculation process order receipts on the calendar date. This is calculated by the MRP process as the quantity, which is expected to be received on the calendar date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 
| [PlannedOrderReleases](Logistics.Inventory.RequisitionPlan.md#plannedorderreleases) | [Quantity](../data-types.md#quantity) | The planned by the calculation process order releases on the specified calendar date. This is calculated by the MRP process as the quantity, which should be released for purchasing, transfer or production on the calendar date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 
| [ProjectedAvailableBalance](Logistics.Inventory.RequisitionPlan.md#projectedavailablebalance) | [Quantity](../data-types.md#quantity) | Expected balance of the product for the calendar date. This is a calculation, based on the current physical inventory and expected future transactions. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 
| [Quantity](Logistics.Inventory.RequisitionPlan.md#quantity) | [Quantity](../data-types.md#quantity) | The Quantity of the purchase orders the program shall generate; the suggested value equals Planned_Order_Releases but can be changed by the user;. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 
| [ReleaseDate](Logistics.Inventory.RequisitionPlan.md#releasedate) | datetime (nullable) | The suggested by the program value equals Calendar_Date; the release date of the purchase orders to be generated. 
| [ScheduledReceipts](Logistics.Inventory.RequisitionPlan.md#scheduledreceipts) | [Quantity](../data-types.md#quantity) | The scheduled receipts of the product on the specified calendar date. This is calculated as the unexecuted quantity of released receipt store orders, whose expected execution date is equal to the calendar date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Logistics.Inventory.RequisitionPlan.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this RequisitionPlan applies, or null if it is for all enterprise companies. [Filter(multi eq)] |
| [FromStore](Logistics.Inventory.RequisitionPlan.md#fromstore) | [Stores](Logistics.Inventory.Stores.md) (nullable) | When the order is for transfer, this is the store from which we shall transfer the product. [Filter(multi eq)] |
| [Product](Logistics.Inventory.RequisitionPlan.md#product) | [Products](General.Products.Products.md) | The product, for which we are planning. [Required] [Filter(multi eq)] |
| [Store](Logistics.Inventory.RequisitionPlan.md#store) | [Stores](Logistics.Inventory.Stores.md) | The store, which is planned. [Required] [Filter(multi eq)] |
| [Supplier](Logistics.Inventory.RequisitionPlan.md#supplier) | [Suppliers](Logistics.Procurement.Suppliers.md) (nullable) | The default supplier in the default product supply for current store, if any. [Filter(multi eq)] |


## Attribute Details

### CalendarDate

> The date for which we are planning. A record is created for each calendar date, on which there are events (orders, executions, planned events, etc.) for the product. Past events are stored on the current date of the planning. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CompletionDate

> The suggested by the program value equals Calendar_Date + Planning_Lead_Time_Days of the default product supply for this store; the completion date of the purchase orders to be generated.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ConfirmAction

> True - generate firm planned orders for the current row; false- do not generate;. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ExplanationMessage

> A message that explains why the program has generated the planned orders for this row.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FirmPlannedOrderReceipts

> The quantity, which is expected to be received on the calendar date. The quantity is the same as the quantity, planned in Firm Planned Order Releases, but at a different calendar date - the expected receivement date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### FirmPlannedOrderReleases

> The order releases which were manually confirmed for release on the specified calendar date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### GenerationDate

> Indicates the date on which the plan is generated. [Required] [Default(Now)]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### GrossRequirements

> The gross requirements of the product on the specified calendar date. This is calculated as the unexecuted quantity of issue store orders, whose expected execution date is equal to the calendar date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  

### NetRequirements

> The net requirements for the date, which are in shortage for the calendar date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PlannedOrderReceipts

> The planned by the calculation process order receipts on the calendar date. This is calculated by the MRP process as the quantity, which is expected to be received on the calendar date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PlannedOrderReleases

> The planned by the calculation process order releases on the specified calendar date. This is calculated by the MRP process as the quantity, which should be released for purchasing, transfer or production on the calendar date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ProjectedAvailableBalance

> Expected balance of the product for the calendar date. This is a calculation, based on the current physical inventory and expected future transactions. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Quantity

> The Quantity of the purchase orders the program shall generate; the suggested value equals Planned_Order_Releases but can be changed by the user;. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ReleaseDate

> The suggested by the program value equals Calendar_Date; the release date of the purchase orders to be generated.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ScheduledReceipts

> The scheduled receipts of the product on the specified calendar date. This is calculated as the unexecuted quantity of released receipt store orders, whose expected execution date is equal to the calendar date. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### EnterpriseCompany

> The Enterprise Company to which this RequisitionPlan applies, or null if it is for all enterprise companies. [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromStore

> When the order is for transfer, this is the store from which we shall transfer the product. [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

> The product, for which we are planning. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

> The store, which is planned. [Required] [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Supplier

> The default supplier in the default product supply for current store, if any. [Filter(multi eq)]

_Type_: **[Suppliers](Logistics.Procurement.Suppliers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Inventory.RequisitionPlan erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.RequisitionPlan erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.RequisitionPlan erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_RequisitionPlan?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_RequisitionPlan?$top=10>

