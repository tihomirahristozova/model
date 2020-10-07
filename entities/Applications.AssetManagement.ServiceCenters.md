# Applications.AssetManagement.ServiceCenters

Contains data about the service centers, which can maintain the assets. Entity: Eam_Service_Centers (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.AssetManagement.ServiceCenters.md#Id) | guid |  
| [Notes](Applications.AssetManagement.ServiceCenters.md#Notes) | string (nullable) | Notes for this ServiceCenter. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Applications.AssetManagement.ServiceCenters.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The enterprise company, whose assets will be maintained by the service center. When null, the service center can maintain assets for all enterprise companies. [Filter(multi eq)] |
| [Party](Applications.AssetManagement.ServiceCenters.md#Party) | [General.Contacts.Parties](General.Contacts.Parties.md) | The person or company, actually performing the maintenance. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this ServiceCenter.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company, whose assets will be maintained by the service center. When null, the service center can maintain assets for all enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Party

> The person or company, actually performing the maintenance. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.ServiceCenters erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.ServiceCenters erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.AssetManagement.ServiceCenters erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ServiceCenters?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ServiceCenters?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Eam_Service_Centers?$top=10>

