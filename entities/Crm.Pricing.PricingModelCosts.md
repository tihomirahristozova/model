---
uid: Crm.Pricing.PricingModelCosts
---
# Crm.Pricing.PricingModelCosts Entity

**Namespace:** [Crm.Pricing](Crm.Pricing.md)  

List of costs, associated with a pricing model. Entity: Crm_Pricing_Model_Costs

## Default Visualization
Default Display Text Format:  
_{PricingModel.Name}_  
Default Search Members:  
_PricingModel.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Crm.Pricing.PricingModels](Crm.Pricing.PricingModels.md)  
Aggregate Root:  
[Crm.Pricing.PricingModels](Crm.Pricing.PricingModels.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AmountPercent](Crm.Pricing.PricingModelCosts.md#amountpercent) | decimal (6, 5) __nullable__ | Used when the cost is calculated as percent of the amount. null when the cost is calculated in a different way. 
| [AmountPerUnit](Crm.Pricing.PricingModelCosts.md#amountperunit) | [Amount (9, 2)](../data-types.md#amount) __nullable__ | Used when the cost is calculated as amount per unit of the product. The unit is defined in Measurement_Unit_Id. null when the cost is calculated in a different way. `Currency: PricingModel.Currency` 
| [Id](Crm.Pricing.PricingModelCosts.md#id) | guid |  
| [LineNo](Crm.Pricing.PricingModelCosts.md#lineno) | int32 | The consequtive number of the cost within the pricing model. `Required` 
| [ObjectVersion](Crm.Pricing.PricingModelCosts.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CostType](Crm.Pricing.PricingModelCosts.md#costtype) | [CostTypes](Finance.Cost.CostTypes.md) | The cost type, which is listed for the pricing model. `Required` `Filter(multi eq)` |
| [MeasurementUnit](Crm.Pricing.PricingModelCosts.md#measurementunit) | [MeasurementUnits](General.MeasurementUnits.md) (nullable) | The measurement unit for which the Amount_Per_Unit is defined. null when the cost is calculated in a different way. `Filter(multi eq)` |
| [PricingModel](Crm.Pricing.PricingModelCosts.md#pricingmodel) | [PricingModels](Crm.Pricing.PricingModels.md) | Pricing model, for which the cost is defined. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### AmountPercent

Used when the cost is calculated as percent of the amount. null when the cost is calculated in a different way.

_Type_: **decimal (6, 5) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### AmountPerUnit

Used when the cost is calculated as amount per unit of the product. The unit is defined in Measurement_Unit_Id. null when the cost is calculated in a different way. `Currency: PricingModel.Currency`

_Type_: **[Amount (9, 2)](../data-types.md#amount) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

The consequtive number of the cost within the pricing model. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.PricingModel.Costs.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.PricingModel.Costs.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### CostType

The cost type, which is listed for the pricing model. `Required` `Filter(multi eq)`

_Type_: **[CostTypes](Finance.Cost.CostTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### MeasurementUnit

The measurement unit for which the Amount_Per_Unit is defined. null when the cost is calculated in a different way. `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PricingModel

Pricing model, for which the cost is defined. `Required` `Filter(multi eq)` `Owner`

_Type_: **[PricingModels](Crm.Pricing.PricingModels.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Pricing.PricingModelCosts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Pricing.PricingModelCosts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pricing_PricingModelCosts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pricing_PricingModelCosts?$top=10>

