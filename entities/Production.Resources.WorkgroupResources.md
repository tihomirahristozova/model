# Production.Resources.WorkgroupResources

Describes the availability of resources in the active workgroups. Entity: Prd_Workgroup_Resources

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Resources.WorkgroupResources.md#Id) | guid |  
| [AvailableQuantity](Production.Resources.WorkgroupResources.md#AvailableQuantity) | [Quantity](../data-types/Quantity.md) | Quantity available of the resource in this workgroup. The measurement unit is specified in Prd_Resources. [Unit: Resource.PrimaryUnit] [Required] [Default(0)] 
| [Notes](Production.Resources.WorkgroupResources.md#Notes) | string (nullable) | User notes for the workgroup resource. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Resource](Production.Resources.WorkgroupResources.md#Resource) | [Production.Resources.Resources](Production.Resources.Resources.md) | The contained resource type. [Required] [Filter(multi eq)] |
| [Workgroup](Production.Resources.WorkgroupResources.md#Workgroup) | [Production.Resources.Workgroups](Production.Resources.Workgroups.md) | Id of the workgroup, containing the resource. [Required] [Filter(multi eq)] [Owner] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Capacity | [Production.Resources.Capacity](Production.Resources.Capacity.md) | List of [Capacity](Production.Resources.Capacity.md) child objects, based on the [Production.Resources.Capacity.WorkgroupResource](Production.Resources.Capacity.md#WorkgroupResource) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AvailableQuantity

> Quantity available of the resource in this workgroup. The measurement unit is specified in Prd_Resources. [Unit: Resource.PrimaryUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Notes

> User notes for the workgroup resource.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Resource

> The contained resource type. [Required] [Filter(multi eq)]

_Type_: **[Production.Resources.Resources](Production.Resources.Resources.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Workgroup

> Id of the workgroup, containing the resource. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.Resources.Workgroups](Production.Resources.Workgroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Production.Resources.WorkgroupResources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.WorkgroupResources erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Resources.WorkgroupResources erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_WorkgroupResources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_WorkgroupResources?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Prd_Workgroup_Resources?$top=10>

