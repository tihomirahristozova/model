---
uid: Applications.Fleet.VehicleSets
---
# Applications.Fleet.VehicleSets

Represents sets of vehicles, which can travel together. Entity: Fleet_Vehicle_Sets

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Fleet.VehicleSets.md#Id) | guid |  
| [Active](Applications.Fleet.VehicleSets.md#Active) | boolean | True if the vehicle set is active for choosing; false - otherwise. [Required] [Default(true)] [Filter(eq)] 
| [Name](Applications.Fleet.VehicleSets.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Name of the vehicle set (Multilanguage). [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Applications.Fleet.VehicleSets.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company operating the vehicle set. [Required] [Filter(multi eq)] [Owner] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Vehicles | [Applications.Fleet.VehicleSetVehicles](Applications.Fleet.VehicleSetVehicles.md) | List of [VehicleSetVehicle](Applications.Fleet.VehicleSetVehicles.md) child objects, based on the [Applications.Fleet.VehicleSetVehicle.VehicleSet](Applications.Fleet.VehicleSetVehicles.md#VehicleSet) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Active

> True if the vehicle set is active for choosing; false - otherwise. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

> Name of the vehicle set (Multilanguage). [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company operating the vehicle set. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Fleet.VehicleSets erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.VehicleSets erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Fleet.VehicleSets erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleSets?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleSets?$top=10>

