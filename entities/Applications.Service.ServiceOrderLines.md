# Applications.Service.ServiceOrderLines

Contains the details and problem symptoms for each object, which requires servicing. Entity: Srv_Service_Order_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceOrderLines.md#Id) | guid |  
| [LineNo](Applications.Service.ServiceOrderLines.md#LineNo) | int32 | Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required] [Filter(eq)] 
| [SymptomDescription](Applications.Service.ServiceOrderLines.md#SymptomDescription) | string (nullable) | Description or synopsis of the symptoms of the failed object. [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ServiceObject](Applications.Service.ServiceOrderLines.md#ServiceObject) | [Applications.Service.ServiceObjects](Applications.Service.ServiceObjects.md) | The service object, which is experiencing the symptoms and needs repair. [Required] [Filter(multi eq)] |
| [ServiceOrder](Applications.Service.ServiceOrderLines.md#ServiceOrder) | [Applications.Service.ServiceOrders](Applications.Service.ServiceOrders.md) | The [ServiceOrder](Applications.Service.ServiceOrderLines.md#ServiceOrder) to which this ServiceOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### LineNo

> Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.ServiceOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.ServiceOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### SymptomDescription

> Description or synopsis of the symptoms of the failed object. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### ServiceObject

> The service object, which is experiencing the symptoms and needs repair. [Required] [Filter(multi eq)]

_Type_: **[Applications.Service.ServiceObjects](Applications.Service.ServiceObjects.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ServiceOrder

> The [ServiceOrder](Applications.Service.ServiceOrderLines.md#ServiceOrder) to which this ServiceOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Service.ServiceOrders](Applications.Service.ServiceOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Service.ServiceOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceOrderLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Service.ServiceOrderLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceOrderLines?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Srv_Service_Order_Lines?$top=10>

