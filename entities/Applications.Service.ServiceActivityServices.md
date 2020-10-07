# Applications.Service.ServiceActivityServices

Contains the services, which were actually performed during the service activity (repair). Entity: Srv_Service_Activity_Services

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceActivityServices.md#Id) | guid |  
| [CoveredByGuarantee](Applications.Service.ServiceActivityServices.md#CoveredByGuarantee) | boolean | True when the performed service is covered by the guarantee. [Required] [Default(false)] 
| [LineNo](Applications.Service.ServiceActivityServices.md#LineNo) | int32 | Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required] 
| [Notes](Applications.Service.ServiceActivityServices.md#Notes) | string (nullable) | Short notes for the service. 
| [Quantity](Applications.Service.ServiceActivityServices.md#Quantity) | [Quantity](../data-types/Quantity.md) | The quantity of the service in the measurement unit of the service. [Unit: Service.MeasurementUnit] [Required] [Default(1)] 
| [ServiceName](Applications.Service.ServiceActivityServices.md#ServiceName) | string | Description of the conducted service. The description may vary (contain additional information) from the standart name of the service. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PerformedByPerson](Applications.Service.ServiceActivityServices.md#PerformedByPerson) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | The id of the person from the enterprise company that actually performed the work. [Filter(multi eq)] |
| [ServiceActivity](Applications.Service.ServiceActivityServices.md#ServiceActivity) | [Applications.Service.ServiceActivities](Applications.Service.ServiceActivities.md) | The [ServiceActivity](Applications.Service.ServiceActivityServices.md#ServiceActivity) to which this ServiceActivityService belongs. [Required] [Filter(multi eq)] [Owner] |
| [Service](Applications.Service.ServiceActivityServices.md#Service) | [Applications.Service.Services](Applications.Service.Services.md) | The type of service that is conducted. [Required] [Filter(multi eq)] |
| [ServiceObject](Applications.Service.ServiceActivityServices.md#ServiceObject) | [Applications.Service.ServiceObjects](Applications.Service.ServiceObjects.md) (nullable) | The service object that was serviced. null means that it is unknown or N/A. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| ServiceActivityAgreedServices | [Applications.Service.ServiceActivityAgreedServices](Applications.Service.ServiceActivityAgreedServices.md) | List of [ServiceActivityAgreedService](Applications.Service.ServiceActivityAgreedServices.md) child objects, based on the [Applications.Service.ServiceActivityAgreedService.ServiceActivityService](Applications.Service.ServiceActivityAgreedServices.md#ServiceActivityService) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CoveredByGuarantee

> True when the performed service is covered by the guarantee. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LineNo

> Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.ServiceActivity.Services.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.ServiceActivity.Services.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### Notes

> Short notes for the service.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Quantity

> The quantity of the service in the measurement unit of the service. [Unit: Service.MeasurementUnit] [Required] [Default(1)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ServiceName

> Description of the conducted service. The description may vary (contain additional information) from the standart name of the service. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Service.Name`

## Reference Details

### PerformedByPerson

> The id of the person from the enterprise company that actually performed the work. [Filter(multi eq)]

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ServiceActivity

> The [ServiceActivity](Applications.Service.ServiceActivityServices.md#ServiceActivity) to which this ServiceActivityService belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Service.ServiceActivities](Applications.Service.ServiceActivities.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Service

> The type of service that is conducted. [Required] [Filter(multi eq)]

_Type_: **[Applications.Service.Services](Applications.Service.Services.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ServiceObject

> The service object that was serviced. null means that it is unknown or N/A. [Filter(multi eq)]

_Type_: **[Applications.Service.ServiceObjects](Applications.Service.ServiceObjects.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.ServiceActivity.DefaultServiceObject`

_Front-End Recalc Expressions:_  
`obj.ServiceActivity.DefaultServiceObject`


## Business Rules

[!list erp.entity=Applications.Service.ServiceActivityServices erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceActivityServices erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Service.ServiceActivityServices erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceActivityServices?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceActivityServices?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Srv_Service_Activity_Services?$top=10>

