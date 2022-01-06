---
uid: Production.Resources.WorkgroupResources
---
# Production.Resources.WorkgroupResources Entity

**Namespace:** [Production.Resources](Production.Resources.md)  

Describes the availability of resources in the active workgroups. Entity: Prd_Workgroup_Resources

## Default Visualization
Default Display Text Format:  
_{Workgroup.Name}_  
Default Search Members:  
_Workgroup.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Production.Resources.Workgroups](Production.Resources.Workgroups.md)  
Aggregate Root:  
[Production.Resources.Workgroups](Production.Resources.Workgroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AvailableQuantity](Production.Resources.WorkgroupResources.md#availablequantity) | [Quantity (18, 3)](../data-types.md#quantity) | Quantity available of the resource in this workgroup. The measurement unit is specified in Prd_Resources. `Unit: Resource.PrimaryUnit` `Required` `Default(0)` 
| [Id](Production.Resources.WorkgroupResources.md#id) | guid |  
| [Notes](Production.Resources.WorkgroupResources.md#notes) | string (254) __nullable__ | User notes for the workgroup resource. 
| [ObjectVersion](Production.Resources.WorkgroupResources.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Resource](Production.Resources.WorkgroupResources.md#resource) | [Resources](Production.Resources.Resources.md) | The contained resource type. `Required` `Filter(multi eq)` |
| [Workgroup](Production.Resources.WorkgroupResources.md#workgroup) | [Workgroups](Production.Resources.Workgroups.md) | Id of the workgroup, containing the resource. `Required` `Filter(multi eq)` `Owner` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Capacity | [Capacity](Production.Resources.Capacity.md) | List of `Capacity`(Production.Resources.Capacity.md) child objects, based on the `Production.Resources.Capacity.WorkgroupResource`(Production.Resources.Capacity.md#workgroupresource) back reference 


## Attribute Details

### AvailableQuantity

Quantity available of the resource in this workgroup. The measurement unit is specified in Prd_Resources. `Unit: Resource.PrimaryUnit` `Required` `Default(0)`

_Type_: **[Quantity (18, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

User notes for the workgroup resource.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### Resource

The contained resource type. `Required` `Filter(multi eq)`

_Type_: **[Resources](Production.Resources.Resources.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Workgroup

Id of the workgroup, containing the resource. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Workgroups](Production.Resources.Workgroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Production.Resources.WorkgroupResources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Production.Resources.WorkgroupResources erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_WorkgroupResources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_WorkgroupResources?$top=10>

