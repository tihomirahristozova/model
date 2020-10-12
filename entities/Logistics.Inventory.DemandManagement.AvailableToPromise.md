---
uid: Logistics.Inventory.DemandManagement.AvailableToPromise
---
# Logistics.Inventory.DemandManagement.AvailableToPromise Entity

Quantities available to promise for the different date periods. Also contains the current and projected availability. Entity: Inv_Demand_Management_ATP

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ATPBase](Logistics.Inventory.DemandManagement.AvailableToPromise.md#atpbase) | [Quantity](../data-types.md#quantity) | Indicates the quantity available to promise (in a base unit). It is valid from this date on. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [CurrentAvailabilityBase](Logistics.Inventory.DemandManagement.AvailableToPromise.md#currentavailabilitybase) | [Quantity](../data-types.md#quantity) | The current availability in а base measurement unit. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [FromDate](Logistics.Inventory.DemandManagement.AvailableToPromise.md#fromdate) | datetime | Тhe date from which the available to promise quantity is valid. [Required] [Filter(eq;ge;le)] 
| [MovementsBase](Logistics.Inventory.DemandManagement.AvailableToPromise.md#movementsbase) | [Quantity](../data-types.md#quantity) | The sum of the quantity of all planned stock movements on this date in а base measurement unit. . [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [MovementsToDateBase](Logistics.Inventory.DemandManagement.AvailableToPromise.md#movementstodatebase) | [Quantity](../data-types.md#quantity) | The sum of the quantity of all planned stock movements until this date (inclusive) in а base measurement unit. The value is cumulative. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [ProjectedAvailabilityBase](Logistics.Inventory.DemandManagement.AvailableToPromise.md#projectedavailabilitybase) | [Quantity](../data-types.md#quantity) | Projected Availability in а base measurement unit on the particular date. The value is cumulative and includes the sum of all planned stock movements until this date (inclusive) and the current availability. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Logistics.Inventory.DemandManagement.AvailableToPromise.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | Тhe Enterprise Company, for which the quantities are calculated. [Required] [Filter(multi eq)] |
| [Product](Logistics.Inventory.DemandManagement.AvailableToPromise.md#product) | [Products](General.Products.Products.md) | The Product, for which the quantities are calculated. [Required] [Filter(multi eq)] |
| [Store](Logistics.Inventory.DemandManagement.AvailableToPromise.md#store) | [Stores](Logistics.Inventory.Stores.md) | The Store, for which the quantities are calculated. [Required] [Filter(multi eq)] |


## Attribute Details

### ATPBase

Indicates the quantity available to promise (in a base unit). It is valid from this date on. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CurrentAvailabilityBase

The current availability in а base measurement unit. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FromDate

Тhe date from which the available to promise quantity is valid. [Required] [Filter(eq;ge;le)]

_Type_: **datetime**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### MovementsBase

The sum of the quantity of all planned stock movements on this date in а base measurement unit. . [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### MovementsToDateBase

The sum of the quantity of all planned stock movements until this date (inclusive) in а base measurement unit. The value is cumulative. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProjectedAvailabilityBase

Projected Availability in а base measurement unit on the particular date. The value is cumulative and includes the sum of all planned stock movements until this date (inclusive) and the current availability. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

Тhe Enterprise Company, for which the quantities are calculated. [Required] [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The Product, for which the quantities are calculated. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

The Store, for which the quantities are calculated. [Required] [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Inventory.DemandManagement.AvailableToPromise erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.DemandManagement.AvailableToPromise erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_DemandManagement_AvailableToPromise?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_DemandManagement_AvailableToPromise?$top=10>

