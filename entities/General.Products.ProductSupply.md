---
uid: General.Products.ProductSupply
---
# General.Products.ProductSupply Entity

**Namespace:** [General.Products](General.Products.md)  

Contains supply rules, which are used by the procurement planning system. Entity: Gen_Product_Supply

## Default Visualization
Default Display Text Format:  
_{BuyerName:T}_  
Default Search Member:  
_BuyerName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Products.ProductSupply](General.Products.ProductSupply.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BuyerName](General.Products.ProductSupply.md#buyername) | string(64) (nullable) | The code or name of the person, who is in charge for purchasing the product from external suppliers. It is used to group different products on purchase demand report. null when Procurement_Type is not buy. 
| [FixedOrderQuantityBase](General.Products.ProductSupply.md#fixedorderquantitybase) | [Quantity](../data-types.md#quantity) | Fixed order quantity under the FOQ & EOQ replenishment system. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Default(0)` 
| [Id](General.Products.ProductSupply.md#id) | guid |  
| [IsActive](General.Products.ProductSupply.md#isactive) | boolean | True if this product supply is active. `Required` `Default(true)` `Filter(eq)` 
| [IsDefault](General.Products.ProductSupply.md#isdefault) | boolean | Specifies whether this is the default supply rule. The planning system works using *only* the default supply rules. The other rules are for reference and user information. `Required` `Default(true)` `Filter(eq)` 
| [ManufacturingPolicy](General.Products.ProductSupply.md#manufacturingpolicy) | [ManufacturingPolicy](General.Products.ProductSupply.md#manufacturingpolicy) | MTS=Make-To-Stock; MTO=Make-To-Order; ATO=Assemble-To-Order;ETO=Engineer-To-Order. `Required` `Default("MTS")` 
| [OrderLotSizeQuantityBase](General.Products.ProductSupply.md#orderlotsizequantitybase) | [Quantity](../data-types.md#quantity) | The quantity of the product, normally ordered from the plant or supplier. The quantity is expressed in the base measurement unit. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Default(1)` 
| [OrderLotSizingMethod](General.Products.ProductSupply.md#orderlotsizingmethod) | [OrderLotSizingMethod](General.Products.ProductSupply.md#orderlotsizingmethod) | LFL=Lot for Lot; FOQ=Fixed order quantity; EOQ=Eqonomic Order Quantity; ROP=ReOrder Point; ROT=ReOrder point with Time planning; LFP = Lot For Period;. `Required` `Default("ROP")` 
| [OrderMaximum](General.Products.ProductSupply.md#ordermaximum) | [Quantity](../data-types.md#quantity) (nullable) | Order maximum when buying or making. null means no maximum. `Unit: Product.BaseMeasurementCategory.BaseUnit` 
| [OrderMinimum](General.Products.ProductSupply.md#orderminimum) | [Quantity](../data-types.md#quantity) | Minimum order quantity both for buying and making. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Default(0)` 
| [OrderMultiple](General.Products.ProductSupply.md#ordermultiple) | boolean | True if the order qty should be multiple of lot size when buying or making. `Required` `Default(false)` 
| [OrderPeriodPlanningDays](General.Products.ProductSupply.md#orderperiodplanningdays) | int32 (nullable) | For how many days in the future should be planned - for fixed period replenishment system. null - not yet specified. 
| [OrderPeriodStartDate](General.Products.ProductSupply.md#orderperiodstartdate) | datetime (nullable) | Start date of the first period under fixed period replenishment system. null - not yet specified. 
| [OrderPointQuantityBase](General.Products.ProductSupply.md#orderpointquantitybase) | [Quantity](../data-types.md#quantity) | Order point quantity under the OP replenishment system. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Default(0)` 
| [OrderPolicy](General.Products.ProductSupply.md#orderpolicy) | [OrderPolicy](General.Products.ProductSupply.md#orderpolicy) | Order policy/replenishment system. OPS=Order Point System; OPT=Order Point System with Time planning; PRS=Periodic Review System/Periods Of Supply; MRP = Material Requirements Planning. `Required` `Default("OPS")` 
| [PlanningAnnual<br />CarryingCostPercent](General.Products.ProductSupply.md#planningannualcarryingcostpercent) | decimal(5, 4) (nullable) | The expected carrying cost as percentage of inventory cost. null means unknown. 
| [PlanningAnnual<br />UsageQuantityBase](General.Products.ProductSupply.md#planningannualusagequantitybase) | [Quantity](../data-types.md#quantity) (nullable) | Average usage of the product for 1 year. NUL means unknown. `Unit: Product.BaseMeasurementCategory.BaseUnit` 
| [PlanningHorizonDays](General.Products.ProductSupply.md#planninghorizondays) | int32 | Number of days in the future for which to plan the demand and supply. `Required` `Default(0)` 
| [PlanningLeadTimeDays](General.Products.ProductSupply.md#planningleadtimedays) | int32 | The number of days required to supply or manufacture the product. The number is exclusive of the lead-time of lower-level components. `Required` `Default(0)` 
| [PlanningMaximum<br />InventoryQuantity<br />Base](General.Products.ProductSupply.md#planningmaximuminventoryquantitybase) | [Quantity](../data-types.md#quantity) (nullable) | Maximum inventory. null if N/A. `Unit: Product.BaseMeasurementCategory.BaseUnit` 
| [PlanningOrderCost<br />BaseCurrency](General.Products.ProductSupply.md#planningordercostbasecurrency) | [Amount](../data-types.md#amount) (nullable) | Projected cost to place an order and set-up equipment. `Currency: EnterpriseCompany.BaseCurrency` 
| [PlanningOrderCycleDays](General.Products.ProductSupply.md#planningordercycledays) | int32 (nullable) | Number of days in one period under fixed period replenishment system. null - not yet specified. 
| [PlanningSafety<br />StockQuantityBase](General.Products.ProductSupply.md#planningsafetystockquantitybase) | [Quantity](../data-types.md#quantity) | Planned lowest inventory level, protecting against unplanned demands. The quantity is expressed in the base measurement unit of the product. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Default(0)` 
| [PlanningTimeFenceDays](General.Products.ProductSupply.md#planningtimefencedays) | int32 | Period in the future inside of which changes to the MPS are carefully evaluated to prevent costly schedule disruption. Demand for the period between DTF and PTF is calculated as the bigger of customer orders and sales forecast. Abbr. - PTF. `Required` `Default(1)` 
| [ProcurementType](General.Products.ProductSupply.md#procurementtype) | [ProcurementType](General.Products.ProductSupply.md#procurementtype) | M=Make; B=Buy; T=Transfer.  Identifies whether the product is produced or externally bought. `Required` `Default("B")` 
| [StandardCostPerLot](General.Products.ProductSupply.md#standardcostperlot) | [Amount](../data-types.md#amount) | Standard cost for one lot of the product. `Currency: Product.CostingCurrency` `Required` `Default(0)` 
| [SupplySchemaId](General.Products.ProductSupply.md#supplyschemaid) | guid (nullable) | The supply schema to use for the distribution of the product among warehouses. `Filter(multi eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultStoreBin](General.Products.ProductSupply.md#defaultstorebin) | [StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | Default store bin for new deliveries using this supply scheme. `Filter(multi eq)` |
| [EnterpriseCompany](General.Products.ProductSupply.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this ProductSupply applies, or null if it is for all enterprise companies. `Filter(multi eq)` |
| [FromStore](General.Products.ProductSupply.md#fromstore) | [Stores](Logistics.Inventory.Stores.md) (nullable) | Used when the Procurement_Type is Transfer. `Filter(multi eq)` |
| [GenerateDocumentType](General.Products.ProductSupply.md#generatedocumenttype) | [DocumentTypes](General.DocumentTypes.md) (nullable) | Specifies the type of the document which should be generated by the procurement planning system, when generating supply based on this rule. `Filter(multi eq)` |
| [PreferredSupplier](General.Products.ProductSupply.md#preferredsupplier) | [Suppliers](Logistics.Procurement.Suppliers.md) (nullable) | Preferred supplier for the product. null if there is no preferred supplier. `Filter(multi eq)` |
| [Product](General.Products.ProductSupply.md#product) | [Products](General.Products.Products.md) (nullable) | The `Product`(General.Products.ProductSupply.md#product) to which this ProductSupply belongs. `Filter(multi eq)` |
| [ProductGroup](General.Products.ProductSupply.md#productgroup) | [ProductGroups](General.Products.ProductGroups.md) (nullable) | Not null when the method is a default method for a whole product group. In this case new products in the group inherit the settings. `Filter(multi eq)` |
| [Store](General.Products.ProductSupply.md#store) | [Stores](Logistics.Inventory.Stores.md) (nullable) | The store for which this rule is defined. When null, the rule is valid for all stores. `Filter(multi eq)` |


## Attribute Details

### BuyerName

The code or name of the person, who is in charge for purchasing the product from external suppliers. It is used to group different products on purchase demand report. null when Procurement_Type is not buy.

_Type_: **string(64) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### FixedOrderQuantityBase

Fixed order quantity under the FOQ & EOQ replenishment system. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Default(0)`

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

True if this product supply is active. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IsDefault

Specifies whether this is the default supply rule. The planning system works using *only* the default supply rules. The other rules are for reference and user information. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### ManufacturingPolicy

MTS=Make-To-Stock; MTO=Make-To-Order; ATO=Assemble-To-Order;ETO=Engineer-To-Order. `Required` `Default("MTS")`

_Type_: **[ManufacturingPolicy](General.Products.ProductSupply.md#manufacturingpolicy)**  
Allowed values for the `ManufacturingPolicy`(General.Products.ProductSupply.md#manufacturingpolicy) data attribute  
_Allowed Values (General.Products.ProductSupplyRepository.ManufacturingPolicy Enum Members)_  

| Value | Description |
| ---- | --- |
| AssembleToOrder | AssembleToOrder value. Stored as 'ATO'. <br /> _Database Value:_ 'ATO' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AssembleToOrder' |
| MakeToOrder | MakeToOrder value. Stored as 'MTO'. <br /> _Database Value:_ 'MTO' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'MakeToOrder' |
| MakeToStock | MakeToStock value. Stored as 'MTS'. <br /> _Database Value:_ 'MTS' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'MakeToStock' |
| EngineerToOrder | EngineerToOrder value. Stored as 'ETO'. <br /> _Database Value:_ 'ETO' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'EngineerToOrder' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **MakeToStock**  

### OrderLotSizeQuantityBase

The quantity of the product, normally ordered from the plant or supplier. The quantity is expressed in the base measurement unit. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Default(1)`

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### OrderLotSizingMethod

LFL=Lot for Lot; FOQ=Fixed order quantity; EOQ=Eqonomic Order Quantity; ROP=ReOrder Point; ROT=ReOrder point with Time planning; LFP = Lot For Period;. `Required` `Default("ROP")`

_Type_: **[OrderLotSizingMethod](General.Products.ProductSupply.md#orderlotsizingmethod)**  
Allowed values for the `OrderLotSizingMethod`(General.Products.ProductSupply.md#orderlotsizingmethod) data attribute  
_Allowed Values (General.Products.ProductSupplyRepository.OrderLotSizingMethod Enum Members)_  

| Value | Description |
| ---- | --- |
| EconomicOrderQuantity | EconomicOrderQuantity value. Stored as 'EOQ'. <br /> _Database Value:_ 'EOQ' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'EconomicOrderQuantity' |
| FixedOrderQuantity | FixedOrderQuantity value. Stored as 'FOQ'. <br /> _Database Value:_ 'FOQ' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'FixedOrderQuantity' |
| LotForLot | LotForLot value. Stored as 'LFL'. <br /> _Database Value:_ 'LFL' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'LotForLot' |
| LotForPeriod | LotForPeriod value. Stored as 'LFP'. <br /> _Database Value:_ 'LFP' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'LotForPeriod' |
| ReorderPoint | ReorderPoint value. Stored as 'ROP'. <br /> _Database Value:_ 'ROP' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'ReorderPoint' |
| ReorderPointWith<br />TimePlanning | ReorderPointWith<br />TimePlanning value. Stored as 'ROT'. <br /> _Database Value:_ 'ROT' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'ReorderPointWith<br />TimePlanning' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **ReorderPoint**  

### OrderMaximum

Order maximum when buying or making. null means no maximum. `Unit: Product.BaseMeasurementCategory.BaseUnit`

_Type_: **[Quantity](../data-types.md#quantity) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrderMinimum

Minimum order quantity both for buying and making. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Default(0)`

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### OrderMultiple

True if the order qty should be multiple of lot size when buying or making. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### OrderPeriodPlanningDays

For how many days in the future should be planned - for fixed period replenishment system. null - not yet specified.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrderPeriodStartDate

Start date of the first period under fixed period replenishment system. null - not yet specified.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrderPointQuantityBase

Order point quantity under the OP replenishment system. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Default(0)`

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### OrderPolicy

Order policy/replenishment system. OPS=Order Point System; OPT=Order Point System with Time planning; PRS=Periodic Review System/Periods Of Supply; MRP = Material Requirements Planning. `Required` `Default("OPS")`

_Type_: **[OrderPolicy](General.Products.ProductSupply.md#orderpolicy)**  
Allowed values for the `OrderPolicy`(General.Products.ProductSupply.md#orderpolicy) data attribute  
_Allowed Values (General.Products.ProductSupplyRepository.OrderPolicy Enum Members)_  

| Value | Description |
| ---- | --- |
| MaterialRequirements<br />Planning | MaterialRequirements<br />Planning value. Stored as 'MRP'. <br /> _Database Value:_ 'MRP' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'MaterialRequirements<br />Planning' |
| OrderPointSystem | OrderPointSystem value. Stored as 'OPS'. <br /> _Database Value:_ 'OPS' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'OrderPointSystem' |
| OrderPointSystem<br />WithTimePlanning | OrderPointSystem<br />WithTimePlanning value. Stored as 'OPT'. <br /> _Database Value:_ 'OPT' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'OrderPointSystem<br />WithTimePlanning' |
| PeriodicReviewSystem | PeriodicReviewSystem value. Stored as 'PRS'. <br /> _Database Value:_ 'PRS' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'PeriodicReviewSystem' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **OrderPointSystem**  

### PlanningAnnualCarryingCostPercent

The expected carrying cost as percentage of inventory cost. null means unknown.

_Type_: **decimal(5, 4) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningAnnualUsageQuantityBase

Average usage of the product for 1 year. NUL means unknown. `Unit: Product.BaseMeasurementCategory.BaseUnit`

_Type_: **[Quantity](../data-types.md#quantity) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningHorizonDays

Number of days in the future for which to plan the demand and supply. `Required` `Default(0)`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### PlanningLeadTimeDays

The number of days required to supply or manufacture the product. The number is exclusive of the lead-time of lower-level components. `Required` `Default(0)`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`IIF( ( Convert( obj.PreferredSupplier.DefaultDeliveryTermDays, Nullable`1) != null), obj.PreferredSupplier.DefaultDeliveryTermDays, obj.PlanningLeadTimeDays)`
### PlanningMaximumInventoryQuantityBase

Maximum inventory. null if N/A. `Unit: Product.BaseMeasurementCategory.BaseUnit`

_Type_: **[Quantity](../data-types.md#quantity) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningOrderCostBaseCurrency

Projected cost to place an order and set-up equipment. `Currency: EnterpriseCompany.BaseCurrency`

_Type_: **[Amount](../data-types.md#amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningOrderCycleDays

Number of days in one period under fixed period replenishment system. null - not yet specified.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningSafetyStockQuantityBase

Planned lowest inventory level, protecting against unplanned demands. The quantity is expressed in the base measurement unit of the product. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Default(0)`

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PlanningTimeFenceDays

Period in the future inside of which changes to the MPS are carefully evaluated to prevent costly schedule disruption. Demand for the period between DTF and PTF is calculated as the bigger of customer orders and sales forecast. Abbr. - PTF. `Required` `Default(1)`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### ProcurementType

M=Make; B=Buy; T=Transfer.  Identifies whether the product is produced or externally bought. `Required` `Default("B")`

_Type_: **[ProcurementType](General.Products.ProductSupply.md#procurementtype)**  
Allowed values for the `ProcurementType`(General.Products.ProductSupply.md#procurementtype) data attribute  
_Allowed Values (General.Products.ProductSupplyRepository.ProcurementType Enum Members)_  

| Value | Description |
| ---- | --- |
| Buy | Buy value. Stored as 'B'. <br /> _Database Value:_ 'B' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Buy' |
| Make | Make value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Make' |
| Transfer | Transfer value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Transfer' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Buy**  

### StandardCostPerLot

Standard cost for one lot of the product. `Currency: Product.CostingCurrency` `Required` `Default(0)`

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### SupplySchemaId

The supply schema to use for the distribution of the product among warehouses. `Filter(multi eq)`

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  


## Reference Details

### DefaultStoreBin

Default store bin for new deliveries using this supply scheme. `Filter(multi eq)`

_Type_: **[StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

The Enterprise Company to which this ProductSupply applies, or null if it is for all enterprise companies. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromStore

Used when the Procurement_Type is Transfer. `Filter(multi eq)`

_Type_: **[Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### GenerateDocumentType

Specifies the type of the document which should be generated by the procurement planning system, when generating supply based on this rule. `Filter(multi eq)`

_Type_: **[DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PreferredSupplier

Preferred supplier for the product. null if there is no preferred supplier. `Filter(multi eq)`

_Type_: **[Suppliers](Logistics.Procurement.Suppliers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The `Product`(General.Products.ProductSupply.md#product) to which this ProductSupply belongs. `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductGroup

Not null when the method is a default method for a whole product group. In this case new products in the group inherit the settings. `Filter(multi eq)`

_Type_: **[ProductGroups](General.Products.ProductGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

The store for which this rule is defined. When null, the rule is valid for all stores. `Filter(multi eq)`

_Type_: **[Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Products.ProductSupply erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.ProductSupply erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductSupply?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductSupply?$top=10>

