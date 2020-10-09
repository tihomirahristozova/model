---
uid: Applications.DataWarehouse.DataValues
---
# Applications.DataWarehouse.DataValues Entity

The actual values in the general data warehouse. Entity: Dw_Data_Values (Introduced in version 18.2)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ActualValue](Applications.DataWarehouse.DataValues.md#actualvalue) | decimal | Accumulates actual value for the measure. [Required] [Default(0)] [Filter(eq)] 
| [Date](Applications.DataWarehouse.DataValues.md#date) | date | The date for which the measure is recorded. All records with dates within each period are summed. [Required] [Filter(eq;ge;le)] 
| [Id](Applications.DataWarehouse.DataValues.md#id) | guid |  
| [TargetValue](Applications.DataWarehouse.DataValues.md#targetvalue) | decimal | Accumulates target value for the measure. [Required] [Default(0)] [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataMeasure](Applications.DataWarehouse.DataValues.md#datameasure) | [DataMeasures](Applications.DataWarehouse.DataMeasures.md) | The measure for which the data is recorded. [Required] [Filter(multi eq)] |
| [EnterpriseCompany](Applications.DataWarehouse.DataValues.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The Enterprise Company for which the data is recorded. [Required] [Filter(multi eq)] |


## Attribute Details

### ActualValue

Accumulates actual value for the measure. [Required] [Default(0)] [Filter(eq)]

_Type_: **decimal**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Date

The date for which the measure is recorded. All records with dates within each period are summed. [Required] [Filter(eq;ge;le)]

_Type_: **date**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### TargetValue

Accumulates target value for the measure. [Required] [Default(0)] [Filter(eq)]

_Type_: **decimal**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### DataMeasure

The measure for which the data is recorded. [Required] [Filter(multi eq)]

_Type_: **[DataMeasures](Applications.DataWarehouse.DataMeasures.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

The Enterprise Company for which the data is recorded. [Required] [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.DataWarehouse.DataValues erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.DataWarehouse.DataValues erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.DataWarehouse.DataValues erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_DataWarehouse_DataValues?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_DataWarehouse_DataValues?$top=10>

