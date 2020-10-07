# Logistics.Wms.WarehouseRequisitionExecutions

Execution ledger for warehouse requisitions. Entity: Wms_Warehouse_Requisition_Executions (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Wms.WarehouseRequisitionExecutions.md#Id) | guid |  
| [CreationTimeUtc](Logistics.Wms.WarehouseRequisitionExecutions.md#CreationTimeUtc) | datetime | The exact time in UTC, when the execution was created in the system. [Required] 
| [Date](Logistics.Wms.WarehouseRequisitionExecutions.md#Date) | date | Date, when the execution occurred in the real world. [Required] 
| [ExecutedQuantity](Logistics.Wms.WarehouseRequisitionExecutions.md#ExecutedQuantity) | decimal | The executed quantity (in the measurement unit of the requisition line). [Required] 
| [IsFinal](Logistics.Wms.WarehouseRequisitionExecutions.md#IsFinal) | boolean | Specifies whether this execution will finalize the execution of the requisition line, regardless of any remaining quantities. [Required] 
| [Time](Logistics.Wms.WarehouseRequisitionExecutions.md#Time) | time | Time, when the execution occurred in the real world. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationUser](Logistics.Wms.WarehouseRequisitionExecutions.md#CreationUser) | [Systems.Security.Users](Systems.Security.Users.md) | The user, who created the record. [Required] [Filter(multi eq)] |
| [WarehouseRequisitionLine](Logistics.Wms.WarehouseRequisitionExecutions.md#WarehouseRequisitionLine) | [Logistics.Wms.WarehouseRequisitionLines](Logistics.Wms.WarehouseRequisitionLines.md) | The requisition line, which is executed. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CreationTimeUtc

> The exact time in UTC, when the execution was created in the system. [Required]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Date

> Date, when the execution occurred in the real world. [Required]

_Type_: **date**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ExecutedQuantity

> The executed quantity (in the measurement unit of the requisition line). [Required]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsFinal

> Specifies whether this execution will finalize the execution of the requisition line, regardless of any remaining quantities. [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Time

> Time, when the execution occurred in the real world. [Required]

_Type_: **time**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CreationUser

> The user, who created the record. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### WarehouseRequisitionLine

> The requisition line, which is executed. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Wms.WarehouseRequisitionLines](Logistics.Wms.WarehouseRequisitionLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Wms.WarehouseRequisitionExecutions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Wms.WarehouseRequisitionExecutions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Wms.WarehouseRequisitionExecutions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseRequisitionExecutions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseRequisitionExecutions?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Wms_Warehouse_Requisition_Executions?$top=10>

