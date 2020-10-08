---
uid: Logistics.Shipment.TransportationExecutionLines
---
# Logistics.Shipment.TransportationExecutionLines

Contains details of executions of transportation order lines. Entity: Log_Transportation_Execution_Lines (Introduced in version 18.2.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Shipment.TransportationExecutionLines.md#Id) | guid |  
| [ExecutionDate](Logistics.Shipment.TransportationExecutionLines.md#ExecutionDate) | date | The date when the operation was executed. [Required] 
| [ExecutionTime](Logistics.Shipment.TransportationExecutionLines.md#ExecutionTime) | time | The time when the operation was executed. [Required] 
| [LineNo](Logistics.Shipment.TransportationExecutionLines.md#LineNo) | int32 | Consecutive line number within this execution. [Required] 
| [Notes](Logistics.Shipment.TransportationExecutionLines.md#Notes) | string (nullable) | Notes for this TransportationExecutionLine. 
| [OperationType](Logistics.Shipment.TransportationExecutionLines.md#OperationType) | [Logistics.Shipment.TransportationExecutionLinesRepository.OperationType](Logistics.Shipment.TransportationExecutionLines.md#OperationType) | The type of operation being executed. L=Loading; U=Unloading; O=Other. [Required] 
| [PalletNumber](Logistics.Shipment.TransportationExecutionLines.md#PalletNumber) | string (nullable) | Pallet number, when applicable. null when unknown or not applicable. 
| [PalletsCount](Logistics.Shipment.TransportationExecutionLines.md#PalletsCount) | int32 (nullable) | Number of pallets affected by this operation. null when unknown or N/A. 
| [VolumeCbm](Logistics.Shipment.TransportationExecutionLines.md#VolumeCbm) | int32 (nullable) | Cargo volume in cubic meters, affected by this operation. null when unknown or N/A. 
| [WeightKg](Logistics.Shipment.TransportationExecutionLines.md#WeightKg) | int32 (nullable) | Cargo weight in kg, affected by this operation. null when unknown or N/A. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ExecutionOfTransportationOrderLine](Logistics.Shipment.TransportationExecutionLines.md#ExecutionOfTransportationOrderLine) | [Logistics.Shipment.TransportationOrderLines](Logistics.Shipment.TransportationOrderLines.md) | The transportation order line, which is executed. [Required] [Filter(multi eq)] |
| [GeoPoint](Logistics.Shipment.TransportationExecutionLines.md#GeoPoint) | [General.Geography.GeoPoints](General.Geography.GeoPoints.md) | The geographic point, where the operation is executed. [Required] [Filter(multi eq)] |
| [TransportationExecution](Logistics.Shipment.TransportationExecutionLines.md#TransportationExecution) | [Logistics.Shipment.TransportationExecutions](Logistics.Shipment.TransportationExecutions.md) | The [TransportationExecution](Logistics.Shipment.TransportationExecutionLines.md#TransportationExecution) to which this TransportationExecutionLine belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ExecutionDate

> The date when the operation was executed. [Required]

_Type_: **date**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.TransportationExecution.ExecutionDate`

_Front-End Recalc Expressions:_  
`obj.TransportationExecution.ExecutionDate`
### ExecutionTime

> The time when the operation was executed. [Required]

_Type_: **time**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.TransportationExecution.ExecutionTime`

_Front-End Recalc Expressions:_  
`obj.TransportationExecution.ExecutionTime`
### LineNo

> Consecutive line number within this execution. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.TransportationExecution.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.TransportationExecution.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### Notes

> Notes for this TransportationExecutionLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OperationType

> The type of operation being executed. L=Loading; U=Unloading; O=Other. [Required]

_Type_: **[Logistics.Shipment.TransportationExecutionLinesRepository.OperationType](Logistics.Shipment.TransportationExecutionLines.md#OperationType)**  
Allowed values for the [OperationType](Logistics.Shipment.TransportationExecutionLines.md#OperationType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Loading | Loading value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Loading' |
| Unloading | Unloading value. Stored as 'U'. <br /> _Database Value:_ 'U' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Unloading' |
| Other | Other value. Stored as 'O'. <br /> _Database Value:_ 'O' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Other' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PalletNumber

> Pallet number, when applicable. null when unknown or not applicable.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PalletsCount

> Number of pallets affected by this operation. null when unknown or N/A.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VolumeCbm

> Cargo volume in cubic meters, affected by this operation. null when unknown or N/A.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### WeightKg

> Cargo weight in kg, affected by this operation. null when unknown or N/A.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ExecutionOfTransportationOrderLine

> The transportation order line, which is executed. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Shipment.TransportationOrderLines](Logistics.Shipment.TransportationOrderLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### GeoPoint

> The geographic point, where the operation is executed. [Required] [Filter(multi eq)]

_Type_: **[General.Geography.GeoPoints](General.Geography.GeoPoints.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.TransportationExecution.GeoPoint`

_Front-End Recalc Expressions:_  
`obj.TransportationExecution.GeoPoint`
### TransportationExecution

> The [TransportationExecution](Logistics.Shipment.TransportationExecutionLines.md#TransportationExecution) to which this TransportationExecutionLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Shipment.TransportationExecutions](Logistics.Shipment.TransportationExecutions.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Shipment.TransportationExecutionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.TransportationExecutionLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Shipment.TransportationExecutionLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_TransportationExecutionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_TransportationExecutionLines?$top=10>

