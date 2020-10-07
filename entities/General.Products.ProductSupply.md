# General.Products.ProductSupply

Contains supply rules, which are used by the procurement planning system. Entity: Gen_Product_Supply

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Products.ProductSupply.md#Id) | guid |  
| [BuyerName](General.Products.ProductSupply.md#BuyerName) | string (nullable) | The code or name of the person, who is in charge for purchasing the product from external suppliers. It is used to group different products on purchase demand report. null when Procurement_Type is not buy. 
| [FixedOrderQuantityBase](General.Products.ProductSupply.md#FixedOrderQuantityBase) | [Quantity](../data-types/Quantity.md) | Fixed order quantity under the FOQ & EOQ replenishment system. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 
| [IsActive](General.Products.ProductSupply.md#IsActive) | boolean | True if this product supply is active. [Required] [Default(true)] [Filter(eq)] 
| [IsDefault](General.Products.ProductSupply.md#IsDefault) | boolean | Specifies whether this is the default supply rule. The planning system works using *only* the default supply rules. The other rules are for reference and user information. [Required] [Default(true)] [Filter(eq)] 
| [ManufacturingPolicy](General.Products.ProductSupply.md#ManufacturingPolicy) | [General.Products.ProductSupplyRepository.ManufacturingPolicy](General.Products.ProductSupply.md#ManufacturingPolicy) | MTS=Make-To-Stock; MTO=Make-To-Order; ATO=Assemble-To-Order;ETO=Engineer-To-Order. [Required] [Default("MTS")] 
| [OrderLotSizeQuantityBase](General.Products.ProductSupply.md#OrderLotSizeQuantityBase) | [Quantity](../data-types/Quantity.md) | The quantity of the product, normally ordered from the plant or supplier. The quantity is expressed in the base measurement unit. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(1)] 
| [OrderLotSizingMethod](General.Products.ProductSupply.md#OrderLotSizingMethod) | [General.Products.ProductSupplyRepository.OrderLotSizingMethod](General.Products.ProductSupply.md#OrderLotSizingMethod) | LFL=Lot for Lot; FOQ=Fixed order quantity; EOQ=Eqonomic Order Quantity; ROP=ReOrder Point; ROT=ReOrder point with Time planning; LFP = Lot For Period;. [Required] [Default("ROP")] 
| [OrderMaximum](General.Products.ProductSupply.md#OrderMaximum) | [Quantity](../data-types/Quantity.md) (nullable) | Order maximum when buying or making. null means no maximum. [Unit: Product.BaseMeasurementCategory.BaseUnit] 
| [OrderMinimum](General.Products.ProductSupply.md#OrderMinimum) | [Quantity](../data-types/Quantity.md) | Minimum order quantity both for buying and making. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 
| [OrderMultiple](General.Products.ProductSupply.md#OrderMultiple) | boolean | True if the order qty should be multiple of lot size when buying or making. [Required] [Default(false)] 
| [OrderPeriodPlanningDays](General.Products.ProductSupply.md#OrderPeriodPlanningDays) | int32 (nullable) | For how many days in the future should be planned - for fixed period replenishment system. null - not yet specified. 
| [OrderPeriodStartDate](General.Products.ProductSupply.md#OrderPeriodStartDate) | datetime (nullable) | Start date of the first period under fixed period replenishment system. null - not yet specified. 
| [OrderPointQuantityBase](General.Products.ProductSupply.md#OrderPointQuantityBase) | [Quantity](../data-types/Quantity.md) | Order point quantity under the OP replenishment system. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 
| [OrderPolicy](General.Products.ProductSupply.md#OrderPolicy) | [General.Products.ProductSupplyRepository.OrderPolicy](General.Products.ProductSupply.md#OrderPolicy) | Order policy/replenishment system. OPS=Order Point System; OPT=Order Point System with Time planning; PRS=Periodic Review System/Periods Of Supply; MRP = Material Requirements Planning. [Required] [Default("OPS")] 
| [PlanningAnnualCarryingCostPercent](General.Products.ProductSupply.md#PlanningAnnualCarryingCostPercent) | decimal (nullable) | The expected carrying cost as percentage of inventory cost. null means unknown. 
| [PlanningAnnualUsageQuantityBase](General.Products.ProductSupply.md#PlanningAnnualUsageQuantityBase) | [Quantity](../data-types/Quantity.md) (nullable) | Average usage of the product for 1 year. NUL means unknown. [Unit: Product.BaseMeasurementCategory.BaseUnit] 
| [PlanningHorizonDays](General.Products.ProductSupply.md#PlanningHorizonDays) | int32 | Number of days in the future for which to plan the demand and supply. [Required] [Default(0)] 
| [PlanningLeadTimeDays](General.Products.ProductSupply.md#PlanningLeadTimeDays) | int32 | The number of days required to supply or manufacture the product. The number is exclusive of the lead-time of lower-level components. [Required] [Default(0)] 
| [PlanningMaximumInventoryQuantityBase](General.Products.ProductSupply.md#PlanningMaximumInventoryQuantityBase) | [Quantity](../data-types/Quantity.md) (nullable) | Maximum inventory. null if N/A. [Unit: Product.BaseMeasurementCategory.BaseUnit] 
| [PlanningOrderCostBaseCurrency](General.Products.ProductSupply.md#PlanningOrderCostBaseCurrency) | [Amount](../data-types/Amount.md) (nullable) | Projected cost to place an order and set-up equipment. [Currency: EnterpriseCompany.BaseCurrency] 
| [PlanningOrderCycleDays](General.Products.ProductSupply.md#PlanningOrderCycleDays) | int32 (nullable) | Number of days in one period under fixed period replenishment system. null - not yet specified. 
| [PlanningSafetyStockQuantityBase](General.Products.ProductSupply.md#PlanningSafetyStockQuantityBase) | [Quantity](../data-types/Quantity.md) | Planned lowest inventory level, protecting against unplanned demands. The quantity is expressed in the base measurement unit of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] 
| [PlanningTimeFenceDays](General.Products.ProductSupply.md#PlanningTimeFenceDays) | int32 | Period in the future inside of which changes to the MPS are carefully evaluated to prevent costly schedule disruption. Demand for the period between DTF and PTF is calculated as the bigger of customer orders and sales forecast. Abbr. - PTF. [Required] [Default(1)] 
| [ProcurementType](General.Products.ProductSupply.md#ProcurementType) | [General.Products.ProductSupplyRepository.ProcurementType](General.Products.ProductSupply.md#ProcurementType) | M=Make; B=Buy; T=Transfer.  Identifies whether the product is produced or externally bought. [Required] [Default("B")] 
| [StandardCostPerLot](General.Products.ProductSupply.md#StandardCostPerLot) | [Amount](../data-types/Amount.md) | Standard cost for one lot of the product. [Currency: Product.CostingCurrency] [Required] [Default(0)] 
| [SupplySchemaId](General.Products.ProductSupply.md#SupplySchemaId) | guid (nullable) | The supply schema to use for the distribution of the product among warehouses. [Filter(multi eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultStoreBin](General.Products.ProductSupply.md#DefaultStoreBin) | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | Default store bin for new deliveries using this supply scheme. [Filter(multi eq)] |
| [EnterpriseCompany](General.Products.ProductSupply.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this ProductSupply applies, or null if it is for all enterprise companies. [Filter(multi eq)] |
| [FromStore](General.Products.ProductSupply.md#FromStore) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | Used when the Procurement_Type is Transfer. [Filter(multi eq)] |
| [GenerateDocumentType](General.Products.ProductSupply.md#GenerateDocumentType) | [General.DocumentTypes](General.DocumentTypes.md) (nullable) | Specifies the type of the document which should be generated by the procurement planning system, when generating supply based on this rule. [Filter(multi eq)] |
| [PreferredSupplier](General.Products.ProductSupply.md#PreferredSupplier) | [Logistics.Procurement.Suppliers](Logistics.Procurement.Suppliers.md) (nullable) | Preferred supplier for the product. null if there is no preferred supplier. [Filter(multi eq)] |
| [ProductGroup](General.Products.ProductSupply.md#ProductGroup) | [General.Products.ProductGroups](General.Products.ProductGroups.md) (nullable) | Not null when the method is a default method for a whole product group. In this case new products in the group inherit the settings. [Filter(multi eq)] |
| [Product](General.Products.ProductSupply.md#Product) | [General.Products.Products](General.Products.Products.md) (nullable) | The [Product](General.Products.ProductSupply.md#Product) to which this ProductSupply belongs. [Filter(multi eq)] |
| [Store](General.Products.ProductSupply.md#Store) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | The store for which this rule is defined. When null, the rule is valid for all stores. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### BuyerName

> The code or name of the person, who is in charge for purchasing the product from external suppliers. It is used to group different products on purchase demand report. null when Procurement_Type is not buy.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FixedOrderQuantityBase

> Fixed order quantity under the FOQ & EOQ replenishment system. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### IsActive

> True if this product supply is active. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IsDefault

> Specifies whether this is the default supply rule. The planning system works using *only* the default supply rules. The other rules are for reference and user information. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### ManufacturingPolicy

> MTS=Make-To-Stock; MTO=Make-To-Order; ATO=Assemble-To-Order;ETO=Engineer-To-Order. [Required] [Default("MTS")]

_Type_: **[General.Products.ProductSupplyRepository.ManufacturingPolicy](General.Products.ProductSupply.md#ManufacturingPolicy)**  
Allowed values for the [ManufacturingPolicy](General.Products.ProductSupply.md#ManufacturingPolicy) data attribute  
_Allowed Values (Enum Members)_  

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

> The quantity of the product, normally ordered from the plant or supplier. The quantity is expressed in the base measurement unit. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(1)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### OrderLotSizingMethod

> LFL=Lot for Lot; FOQ=Fixed order quantity; EOQ=Eqonomic Order Quantity; ROP=ReOrder Point; ROT=ReOrder point with Time planning; LFP = Lot For Period;. [Required] [Default("ROP")]

_Type_: **[General.Products.ProductSupplyRepository.OrderLotSizingMethod](General.Products.ProductSupply.md#OrderLotSizingMethod)**  
Allowed values for the [OrderLotSizingMethod](General.Products.ProductSupply.md#OrderLotSizingMethod) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| EconomicOrderQuantity | EconomicOrderQuantity value. Stored as 'EOQ'. <br /> _Database Value:_ 'EOQ' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'EconomicOrderQuantity' |
| FixedOrderQuantity | FixedOrderQuantity value. Stored as 'FOQ'. <br /> _Database Value:_ 'FOQ' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'FixedOrderQuantity' |
| LotForLot | LotForLot value. Stored as 'LFL'. <br /> _Database Value:_ 'LFL' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'LotForLot' |
| LotForPeriod | LotForPeriod value. Stored as 'LFP'. <br /> _Database Value:_ 'LFP' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'LotForPeriod' |
| ReorderPoint | ReorderPoint value. Stored as 'ROP'. <br /> _Database Value:_ 'ROP' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'ReorderPoint' |
| ReorderPointWithTimePlanning | ReorderPointWithTimePlanning value. Stored as 'ROT'. <br /> _Database Value:_ 'ROT' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'ReorderPointWithTimePlanning' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **ReorderPoint**  

### OrderMaximum

> Order maximum when buying or making. null means no maximum. [Unit: Product.BaseMeasurementCategory.BaseUnit]

_Type_: **[Quantity](../data-types/Quantity.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrderMinimum

> Minimum order quantity both for buying and making. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### OrderMultiple

> True if the order qty should be multiple of lot size when buying or making. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### OrderPeriodPlanningDays

> For how many days in the future should be planned - for fixed period replenishment system. null - not yet specified.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrderPeriodStartDate

> Start date of the first period under fixed period replenishment system. null - not yet specified.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrderPointQuantityBase

> Order point quantity under the OP replenishment system. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### OrderPolicy

> Order policy/replenishment system. OPS=Order Point System; OPT=Order Point System with Time planning; PRS=Periodic Review System/Periods Of Supply; MRP = Material Requirements Planning. [Required] [Default("OPS")]

_Type_: **[General.Products.ProductSupplyRepository.OrderPolicy](General.Products.ProductSupply.md#OrderPolicy)**  
Allowed values for the [OrderPolicy](General.Products.ProductSupply.md#OrderPolicy) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| MaterialRequirementsPlanning | MaterialRequirementsPlanning value. Stored as 'MRP'. <br /> _Database Value:_ 'MRP' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'MaterialRequirementsPlanning' |
| OrderPointSystem | OrderPointSystem value. Stored as 'OPS'. <br /> _Database Value:_ 'OPS' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'OrderPointSystem' |
| OrderPointSystemWithTimePlanning | OrderPointSystemWithTimePlanning value. Stored as 'OPT'. <br /> _Database Value:_ 'OPT' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'OrderPointSystemWithTimePlanning' |
| PeriodicReviewSystem | PeriodicReviewSystem value. Stored as 'PRS'. <br /> _Database Value:_ 'PRS' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'PeriodicReviewSystem' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **OrderPointSystem**  

### PlanningAnnualCarryingCostPercent

> The expected carrying cost as percentage of inventory cost. null means unknown.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningAnnualUsageQuantityBase

> Average usage of the product for 1 year. NUL means unknown. [Unit: Product.BaseMeasurementCategory.BaseUnit]

_Type_: **[Quantity](../data-types/Quantity.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningHorizonDays

> Number of days in the future for which to plan the demand and supply. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### PlanningLeadTimeDays

> The number of days required to supply or manufacture the product. The number is exclusive of the lead-time of lower-level components. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`IIF((Convert(obj.PreferredSupplier.DefaultDeliveryTermDays, Nullable`1) != null), obj.PreferredSupplier.DefaultDeliveryTermDays, obj.PlanningLeadTimeDays)`
### PlanningMaximumInventoryQuantityBase

> Maximum inventory. null if N/A. [Unit: Product.BaseMeasurementCategory.BaseUnit]

_Type_: **[Quantity](../data-types/Quantity.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningOrderCostBaseCurrency

> Projected cost to place an order and set-up equipment. [Currency: EnterpriseCompany.BaseCurrency]

_Type_: **[Amount](../data-types/Amount.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningOrderCycleDays

> Number of days in one period under fixed period replenishment system. null - not yet specified.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningSafetyStockQuantityBase

> Planned lowest inventory level, protecting against unplanned demands. The quantity is expressed in the base measurement unit of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PlanningTimeFenceDays

> Period in the future inside of which changes to the MPS are carefully evaluated to prevent costly schedule disruption. Demand for the period between DTF and PTF is calculated as the bigger of customer orders and sales forecast. Abbr. - PTF. [Required] [Default(1)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### ProcurementType

> M=Make; B=Buy; T=Transfer.  Identifies whether the product is produced or externally bought. [Required] [Default("B")]

_Type_: **[General.Products.ProductSupplyRepository.ProcurementType](General.Products.ProductSupply.md#ProcurementType)**  
Allowed values for the [ProcurementType](General.Products.ProductSupply.md#ProcurementType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Buy | Buy value. Stored as 'B'. <br /> _Database Value:_ 'B' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Buy' |
| Make | Make value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Make' |
| Transfer | Transfer value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Transfer' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Buy**  

### StandardCostPerLot

> Standard cost for one lot of the product. [Currency: Product.CostingCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types/Amount.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### SupplySchemaId

> The supply schema to use for the distribution of the product among warehouses. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### DefaultStoreBin

> Default store bin for new deliveries using this supply scheme. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> The Enterprise Company to which this ProductSupply applies, or null if it is for all enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### FromStore

> Used when the Procurement_Type is Transfer. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### GenerateDocumentType

> Specifies the type of the document which should be generated by the procurement planning system, when generating supply based on this rule. [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PreferredSupplier

> Preferred supplier for the product. null if there is no preferred supplier. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.Suppliers](Logistics.Procurement.Suppliers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProductGroup

> Not null when the method is a default method for a whole product group. In this case new products in the group inherit the settings. [Filter(multi eq)]

_Type_: **[General.Products.ProductGroups](General.Products.ProductGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The [Product](General.Products.ProductSupply.md#Product) to which this ProductSupply belongs. [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Store

> The store for which this rule is defined. When null, the rule is valid for all stores. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Products.ProductSupply erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.ProductSupply erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Products.ProductSupply erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductSupply?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductSupply?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Product_Supply?$top=10>

