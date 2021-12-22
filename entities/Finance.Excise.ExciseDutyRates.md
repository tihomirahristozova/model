---
uid: Finance.Excise.ExciseDutyRates
---
# Finance.Excise.ExciseDutyRates Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

Duty rates are specified by the taxation and customs authorities. They are the basis for the calculation of the excise amount (based on the calculation algorithm, specified in the Product Category). Entity: Exc_Excise_Duty_Rates (Introduced in version 21.1.3.87)

## Default Visualization
Default Display Text Format:  
_{Id}: {ObjectVersion}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Excise.ExciseDutyRates](Finance.Excise.ExciseDutyRates.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ExciseDutyRateField](Finance.Excise.ExciseDutyRates.md#excisedutyratefield) | decimal (10, 6) | The rate which should be applied for the specified product and purpose. `Required` `Default(0)` `Filter(eq;ge;le)` 
| [Id](Finance.Excise.ExciseDutyRates.md#id) | guid |  
| [Notes](Finance.Excise.ExciseDutyRates.md#notes) | string (max) __nullable__ | Notes for this ExciseDutyRate. 
| [ObjectVersion](Finance.Excise.ExciseDutyRates.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ExciseMeasurementUnit](Finance.Excise.ExciseDutyRates.md#excisemeasurementunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit which should be used in the excise calculation. This is only for verification purposes. `Required` `Filter(multi eq)` |
| [ExciseProduct](Finance.Excise.ExciseDutyRates.md#exciseproduct) | [ExciseProducts](Finance.Excise.ExciseProducts.md) | The excise product for which the rate is applied. `Required` `Filter(multi eq)` |
| [ExcisePurposeCode](Finance.Excise.ExciseDutyRates.md#excisepurposecode) | [ExcisePurposeCodes](Finance.Excise.ExcisePurposeCodes.md) | The purpose for which the rate is applied. `Required` `Filter(multi eq)` |


## Attribute Details

### ExciseDutyRateField

The rate which should be applied for the specified product and purpose. `Required` `Default(0)` `Filter(eq;ge;le)`

_Type_: **decimal (10, 6)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this ExciseDutyRate.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### ExciseMeasurementUnit

The measurement unit which should be used in the excise calculation. This is only for verification purposes. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ExciseProduct

The excise product for which the rate is applied. `Required` `Filter(multi eq)`

_Type_: **[ExciseProducts](Finance.Excise.ExciseProducts.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ExcisePurposeCode

The purpose for which the rate is applied. `Required` `Filter(multi eq)`

_Type_: **[ExcisePurposeCodes](Finance.Excise.ExcisePurposeCodes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExciseDutyRates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExciseDutyRates erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Excise_ExciseDutyRates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Excise_ExciseDutyRates?$top=10>

