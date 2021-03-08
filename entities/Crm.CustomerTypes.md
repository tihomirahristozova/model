---
uid: Crm.CustomerTypes
---
# Crm.CustomerTypes Entity

**Namespace:** [Crm](Crm.md)  

User defined customer type. Primarily used for customer definition security, because it has record level security, which is also applied to the individual customer definitions. Entity: Crm_Customer_Types

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.CustomerTypes](Crm.CustomerTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.CustomerTypes.md#id) | guid |  
| [Name](Crm.CustomerTypes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this CustomerType. `Required` `Filter(eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Crm.CustomerTypes.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this CustomerType. Null means that all users have unlimited permissions. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this CustomerType. `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

The access key, containing the user permissions for this CustomerType. Null means that all users have unlimited permissions. `Filter(multi eq)`

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.CustomerTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.CustomerTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_CustomerTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_CustomerTypes?$top=10>

