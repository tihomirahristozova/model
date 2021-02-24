---
uid: Logistics.Shipment.TransportationExecutionLines
---
# Logistics.Shipment.TransportationExecutionLines Entity

**Namespace:** [Logistics.Shipment](Logistics.Shipment.md)  

Contains details of executions of transportation order lines. Entity: Log_Transportation_Execution_Lines (Introduced in version 18.2)

## Default Visualization
Default Display Text Format:  
_{TransportationExecution.DocumentType.Code}:{TransportationExecution.DocumentNo}:{LineNo} - {TransportationExecution.DocumentType.TypeName:T}_  
Default Search Member:  
_TransportationExecution.DocumentNo_  

## Aggregate
  @aggregates  
Aggregate Parent:  
[Logistics.Shipment.TransportationExecutions](Logistics.Shipment.TransportationExecutions.md)  
Aggregate Root:  
[Logistics.Shipment.TransportationExecutions](Logistics.Shipment.TransportationExecutions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ExecutionDate](Logistics.Shipment.TransportationExecutionLines.md#executiondate) | date | The date when the operation was executed. [Required] 
| [ExecutionTime](Logistics.Shipment.TransportationExecutionLines.md#executiontime) | time | The time when the operation was executed. [Required] 
| [Id](Logistics.Shipment.TransportationExecutionLines.md#id) | guid |  
| [LineNo](Logistics.Shipment.TransportationExecutionLines.md#lineno) | int32 | Consecutive line number within this execution. [Required] 
| [Notes](Logistics.Shipment.TransportationExecutionLines.md#notes) | string (nullable) | Notes for this Transportation<br />ExecutionLine. 
| [OperationType](Logistics.Shipment.TransportationExecutionLines.md#operationtype) | [OperationType](Logistics.Shipment.TransportationExecutionLines.md#operationtype) | The type of operation being executed. L=Loading; U=Unloading; O=Other. [Required] 
| [PalletNumber](Logistics.Shipment.TransportationExecutionLines.md#palletnumber) | string (nullable) | Pallet number, when applicable. null when unknown or not applicable. 
| [PalletsCount](Logistics.Shipment.TransportationExecutionLines.md#palletscount) | int32 (nullable) | Number of pallets affected by this operation. null when unknown or N/A. 
| [VolumeCbm](Logistics.Shipment.TransportationExecutionLines.md#volumecbm) | int32 (nullable) | Cargo volume in cubic meters, affected by this operation. null when unknown or N/A. 
| [WeightKg](Logistics.Shipment.TransportationExecutionLines.md#weightkg) | int32 (nullable) | Cargo weight in kg, affected by this operation. null when unknown or N/A. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Logistics.Shipment.TransportationExecutionLines.md#document) | [TransportationExecutions](Logistics.Shipment.TransportationExecutions.md) | The [TransportationExecution](Logistics.Shipment.Transportation<br />ExecutionLines.md#transportationexecution) to which this Transportation<br />ExecutionLine belongs. [Required] [Filter(multi eq)] |
| [ExecutionOfTransportation<br />OrderLine](Logistics.Shipment.TransportationExecutionLines.md#executionoftransportationorderline) | [TransportationOrderLines](Logistics.Shipment.TransportationOrderLines.md) | The transportation order line, which is executed. [Required] [Filter(multi eq)] |
| [GeoPoint](Logistics.Shipment.TransportationExecutionLines.md#geopoint) | [GeoPoints](General.Geography.GeoPoints.md) | The geographic point, where the operation is executed. [Required] [Filter(multi eq)] |
| [TransportationExecution](Logistics.Shipment.TransportationExecutionLines.md#transportationexecution) | [TransportationExecutions](Logistics.Shipment.TransportationExecutions.md) | The [TransportationExecution](Logistics.Shipment.Transportation<br />ExecutionLines.md#transportationexecution) to which this Transportation<br />ExecutionLine belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### ExecutionDate

The date when the operation was executed. [Required]

_Type_: **date**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.TransportationExecution.ExecutionDate`

_Front-End Recalc Expressions:_  
`obj.TransportationExecution.ExecutionDate`
### ExecutionTime

The time when the operation was executed. [Required]

_Type_: **time**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.TransportationExecution.ExecutionTime`

_Front-End Recalc Expressions:_  
`obj.TransportationExecution.ExecutionTime`
### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive line number within this execution. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.TransportationExecution.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.TransportationExecution.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this TransportationExecutionLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OperationType

The type of operation being executed. L=Loading; U=Unloading; O=Other. [Required]

_Type_: **[OperationType](Logistics.Shipment.TransportationExecutionLines.md#operationtype)**  
Allowed values for the [OperationType](Logistics.Shipment.TransportationExecutionLines.md#operationtype) data attribute  
_Allowed Values (Logistics.Shipment.TransportationExecutionLinesRepository.OperationType Enum Members)_  

| Value | Description |
| ---- | --- |
| Loading | Loading value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Loading' |
| Unloading | Unloading value. Stored as 'U'. <br /> _Database Value:_ 'U' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Unloading' |
| Other | Other value. Stored as 'O'. <br /> _Database Value:_ 'O' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Other' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PalletNumber

Pallet number, when applicable. null when unknown or not applicable.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PalletsCount

Number of pallets affected by this operation. null when unknown or N/A.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VolumeCbm

Cargo volume in cubic meters, affected by this operation. null when unknown or N/A.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### WeightKg

Cargo weight in kg, affected by this operation. null when unknown or N/A.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Document

The [TransportationExecution](Logistics.Shipment.TransportationExecutionLines.md#transportationexecution) to which this TransportationExecutionLine belongs. [Required] [Filter(multi eq)]

_Type_: **[TransportationExecutions](Logistics.Shipment.TransportationExecutions.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ExecutionOfTransportationOrderLine

The transportation order line, which is executed. [Required] [Filter(multi eq)]

_Type_: **[TransportationOrderLines](Logistics.Shipment.TransportationOrderLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### GeoPoint

The geographic point, where the operation is executed. [Required] [Filter(multi eq)]

_Type_: **[GeoPoints](General.Geography.GeoPoints.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.TransportationExecution.GeoPoint`

_Front-End Recalc Expressions:_  
`obj.TransportationExecution.GeoPoint`
### TransportationExecution

The [TransportationExecution](Logistics.Shipment.TransportationExecutionLines.md#transportationexecution) to which this TransportationExecutionLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[TransportationExecutions](Logistics.Shipment.TransportationExecutions.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Shipment.TransportationExecutionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.TransportationExecutionLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_TransportationExecutionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_TransportationExecutionLines?$top=10>

