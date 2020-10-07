# Logistics.Inventory.DemandManagement.AvailableToPromiseByLots

Quantities available to promise for the different date periods. Also contains the current and projected availability. The algorithm accounts for the quantities for each lot and separately for the quantities without lot. Entity: Inv_Demand_Management_ATP_By_Lots

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ATPBase](Logistics.Inventory.DemandManagement.AvailableToPromiseByLots.md#ATPBase) | [Quantity](../data-types/Quantity.md) | Indicates the quantity available to promise (in a base unit). It is valid from this date on. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [CurrentAvailabilityBase](Logistics.Inventory.DemandManagement.AvailableToPromiseByLots.md#CurrentAvailabilityBase) | [Quantity](../data-types/Quantity.md) | The current availability in а base measurement unit. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [FromDate](Logistics.Inventory.DemandManagement.AvailableToPromiseByLots.md#FromDate) | datetime | Тhe date from which the available to promise quantity is valid. [Required] [Filter(eq;ge;le)] 
| [MovementsBase](Logistics.Inventory.DemandManagement.AvailableToPromiseByLots.md#MovementsBase) | [Quantity](../data-types/Quantity.md) | The sum of the quantity of all planned stock movements on this date in а base measurement unit. . [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [MovementsToDateBase](Logistics.Inventory.DemandManagement.AvailableToPromiseByLots.md#MovementsToDateBase) | [Quantity](../data-types/Quantity.md) | The sum of the quantity of all planned stock movements until this date (inclusive) in а base measurement unit. The value is cumulative. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [ProjectedAvailabilityBase](Logistics.Inventory.DemandManagement.AvailableToPromiseByLots.md#ProjectedAvailabilityBase) | [Quantity](../data-types/Quantity.md) | Projected Availability in а base measurement unit on the particular date. The value is cumulative and includes the sum of all planned stock movements until this date (inclusive) and the current availability. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Logistics.Inventory.DemandManagement.AvailableToPromiseByLots.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | Тhe Enterprise Company, for which the quantities are calculated. [Required] [Filter(multi eq)] |
| [Lot](Logistics.Inventory.DemandManagement.AvailableToPromiseByLots.md#Lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | The Lot, for which the quantities are calculated. [Filter(multi eq)] |
| [Product](Logistics.Inventory.DemandManagement.AvailableToPromiseByLots.md#Product) | [General.Products.Products](General.Products.Products.md) | The Product, for which the quantities are calculated. [Required] [Filter(multi eq)] |
| [Store](Logistics.Inventory.DemandManagement.AvailableToPromiseByLots.md#Store) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) | The Store, for which the quantities are calculated. [Required] [Filter(multi eq)] |


## Attribute Details

### ATPBase

> Indicates the quantity available to promise (in a base unit). It is valid from this date on. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CurrentAvailabilityBase

> The current availability in а base measurement unit. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FromDate

> Тhe date from which the available to promise quantity is valid. [Required] [Filter(eq;ge;le)]

_Type_: **datetime**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### MovementsBase

> The sum of the quantity of all planned stock movements on this date in а base measurement unit. . [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### MovementsToDateBase

> The sum of the quantity of all planned stock movements until this date (inclusive) in а base measurement unit. The value is cumulative. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProjectedAvailabilityBase

> Projected Availability in а base measurement unit on the particular date. The value is cumulative and includes the sum of all planned stock movements until this date (inclusive) and the current availability. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> Тhe Enterprise Company, for which the quantities are calculated. [Required] [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Lot

> The Lot, for which the quantities are calculated. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The Product, for which the quantities are calculated. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Store

> The Store, for which the quantities are calculated. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.DemandManagement.AvailableToPromiseByLots erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.DemandManagement.AvailableToPromiseByLots erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.DemandManagement.AvailableToPromiseByLots erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_DemandManagement_AvailableToPromiseByLots?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_DemandManagement_AvailableToPromiseByLots?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Inv_Demand_Management_ATP_By_Lots?$top=10>

