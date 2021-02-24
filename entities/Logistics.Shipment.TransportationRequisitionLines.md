---
uid: Logistics.Shipment.TransportationRequisitionLines
---
# Logistics.Shipment.TransportationRequisitionLines Entity

One line in a client requisition for transportation. Different lines usually represent requisitions for different cargo types. Entity: Log_Transportation_Requisition_Lines

Default Display Text Format:  
_{TransportationRequisition.DocumentType.Code}:{TransportationRequisition.DocumentNo}:{LineNo} - {TransportationRequisition.DocumentType.TypeName:T}_  
Default Search Member:  
_TransportationRequisition.DocumentNo_  

[Aggregate](xref:aggregates) Parent:  
[Logistics.Shipment.TransportationRequisitions](Logistics.Shipment.TransportationRequisitions.md)  
[Aggregate](xref:aggregates) Root:  
[Logistics.Shipment.TransportationRequisitions](Logistics.Shipment.TransportationRequisitions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ContentsDescription](Logistics.Shipment.TransportationRequisitionLines.md#contentsdescription) | string | Textual description of the cargo contents. [Required] 
| [Id](Logistics.Shipment.TransportationRequisitionLines.md#id) | guid |  
| [LineNo](Logistics.Shipment.TransportationRequisitionLines.md#lineno) | int32 | Line number, unique within the TransportationRequisition. Usually is increasing number like 10, 20, 30, ... when initially entering the TransportationRequisition (in order to allow insertions with adjustment documents). [Required] [Filter(eq)] 
| [PalletsCount](Logistics.Shipment.TransportationRequisitionLines.md#palletscount) | int32 (nullable) | Number of palettes comprising the cargo. null when it is unknown. 
| [ParentLineNo](Logistics.Shipment.TransportationRequisitionLines.md#parentlineno) | int32 (nullable) | The number of the line within the parent document, which the current line executes. null when the current line does not execute another line. [Filter(eq)] 
| [VolumeCbm](Logistics.Shipment.TransportationRequisitionLines.md#volumecbm) | int32 (nullable) | The volume of the cargo, in CBM (cubic meters). null when it is unknown. 
| [WeightKg](Logistics.Shipment.TransportationRequisitionLines.md#weightkg) | int32 (nullable) | The weight of the cargo, in KG (kilogramms). null when it is unknown. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CargoType](Logistics.Shipment.TransportationRequisitionLines.md#cargotype) | [CargoTypes](Logistics.Shipment.CargoTypes.md) | The type of the transported cargo. [Required] [Filter(multi eq)] |
| [Document](Logistics.Shipment.TransportationRequisitionLines.md#document) | [TransportationRequisitions](Logistics.Shipment.TransportationRequisitions.md) | The [Transportation<br />Requisition](Logistics.Shipment.Transportation<br />RequisitionLines.md#transportationrequisition) to which this Transportation<br />RequisitionLine belongs. [Required] [Filter(multi eq)] |
| [ParentDocument](Logistics.Shipment.TransportationRequisitionLines.md#parentdocument) | [Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] |
| [TransportationRequisition](Logistics.Shipment.TransportationRequisitionLines.md#transportationrequisition) | [TransportationRequisitions](Logistics.Shipment.TransportationRequisitions.md) | The [Transportation<br />Requisition](Logistics.Shipment.Transportation<br />RequisitionLines.md#transportationrequisition) to which this Transportation<br />RequisitionLine belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### ContentsDescription

Textual description of the cargo contents. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Line number, unique within the TransportationRequisition. Usually is increasing number like 10, 20, 30, ... when initially entering the TransportationRequisition (in order to allow insertions with adjustment documents). [Required] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.TransportationRequisition.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.TransportationRequisition.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### PalletsCount

Number of palettes comprising the cargo. null when it is unknown.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentLineNo

The number of the line within the parent document, which the current line executes. null when the current line does not execute another line. [Filter(eq)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### VolumeCbm

The volume of the cargo, in CBM (cubic meters). null when it is unknown.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### WeightKg

The weight of the cargo, in KG (kilogramms). null when it is unknown.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CargoType

The type of the transported cargo. [Required] [Filter(multi eq)]

_Type_: **[CargoTypes](Logistics.Shipment.CargoTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Document

The [TransportationRequisition](Logistics.Shipment.TransportationRequisitionLines.md#transportationrequisition) to which this TransportationRequisitionLine belongs. [Required] [Filter(multi eq)]

_Type_: **[TransportationRequisitions](Logistics.Shipment.TransportationRequisitions.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ParentDocument

The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)]

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportationRequisition

The [TransportationRequisition](Logistics.Shipment.TransportationRequisitionLines.md#transportationrequisition) to which this TransportationRequisitionLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[TransportationRequisitions](Logistics.Shipment.TransportationRequisitions.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Shipment.TransportationRequisitionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.TransportationRequisitionLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_TransportationRequisitionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_TransportationRequisitionLines?$top=10>

