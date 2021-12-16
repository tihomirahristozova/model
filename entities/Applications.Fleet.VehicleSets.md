---
uid: Applications.Fleet.VehicleSets
---
# Applications.Fleet.VehicleSets Entity

**Namespace:** [Applications.Fleet](Applications.Fleet.md)  

Represents sets of vehicles, which can travel together. Entity: Fleet_Vehicle_Sets

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.EnterpriseCompanies](General.EnterpriseCompanies.md)  
Aggregate Root:  
[General.EnterpriseCompanies](General.EnterpriseCompanies.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Active](Applications.Fleet.VehicleSets.md#active) | boolean | True if the vehicle set is active for choosing; false - otherwise. `Required` `Default(true)` `Filter(eq)` 
| [Id](Applications.Fleet.VehicleSets.md#id) | guid |  
| [Name](Applications.Fleet.VehicleSets.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the vehicle set (Multilanguage). `Required` `Filter(eq;like)` 
| [RowVersion](Applications.Fleet.VehicleSets.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Applications.Fleet.VehicleSets.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company operating the vehicle set. `Required` `Filter(multi eq)` `Owner` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Vehicles | [VehicleSetVehicles](Applications.Fleet.VehicleSetVehicles.md) | List of `VehicleSetVehicle`(Applications.Fleet.VehicleSetVehicles.md) child objects, based on the `Applications.Fleet.VehicleSetVehicle.VehicleSet`(Applications.Fleet.VehicleSetVehicles.md#vehicleset) back reference 


## Attribute Details

### Active

True if the vehicle set is active for choosing; false - otherwise. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the vehicle set (Multilanguage). `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

The enterprise company operating the vehicle set. `Required` `Filter(multi eq)` `Owner`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Applications.Fleet.VehicleSets erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Fleet.VehicleSets erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleSets?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleSets?$top=10>

