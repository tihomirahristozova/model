---
uid: Projects.TypeWorkTypes
---
# Projects.TypeWorkTypes Entity

Contains the work types, that can be performed in projects of this project type. Entity: Prj_Type_Work_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.TypeWorkTypes.md#id) | guid |  
| [IsActive](Projects.TypeWorkTypes.md#isactive) | boolean | True when the work type is currently active and selectable in new documents. [Required] [Default(true)] [Filter(eq)] 
| [WorkTypeName](Projects.TypeWorkTypes.md#worktypename) | string | The name of the work type. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [BilledWithProduct](Projects.TypeWorkTypes.md#billedwithproduct) | [Products](General.Products.Products.md) (nullable) | The product, which is used for billing purposes for this work type. The price of the product is also used for project budgeting. null means that the work type cannot be billed. [Filter(multi eq)] |
| [ProjectType](Projects.TypeWorkTypes.md#projecttype) | [ProjectTypes](Projects.ProjectTypes.md) | The [ProjectType](Projects.TypeWorkTypes.md#projecttype) to which this TypeWorkType belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

True when the work type is currently active and selectable in new documents. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### WorkTypeName

The name of the work type. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### BilledWithProduct

The product, which is used for billing purposes for this work type. The price of the product is also used for project budgeting. null means that the work type cannot be billed. [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProjectType

The [ProjectType](Projects.TypeWorkTypes.md#projecttype) to which this TypeWorkType belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[ProjectTypes](Projects.ProjectTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Projects.TypeWorkTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.TypeWorkTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.TypeWorkTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_TypeWorkTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_TypeWorkTypes?$top=10>

