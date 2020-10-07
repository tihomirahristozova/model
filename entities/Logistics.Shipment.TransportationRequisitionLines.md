# Logistics.Shipment.TransportationRequisitionLines

One line in a client requisition for transportation. Different lines usually represent requisitions for different cargo types. Entity: Log_Transportation_Requisition_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Shipment.TransportationRequisitionLines.md#Id) | guid |  
| [ContentsDescription](Logistics.Shipment.TransportationRequisitionLines.md#ContentsDescription) | string | Textual description of the cargo contents. [Required] 
| [LineNo](Logistics.Shipment.TransportationRequisitionLines.md#LineNo) | int32 | Line number, unique within the TransportationRequisition. Usually is increasing number like 10, 20, 30, ... when initially entering the TransportationRequisition (in order to allow insertions with adjustment documents). [Required] [Filter(eq)] 
| [PalletsCount](Logistics.Shipment.TransportationRequisitionLines.md#PalletsCount) | int32 (nullable) | Number of palettes comprising the cargo. null when it is unknown. 
| [ParentLineNo](Logistics.Shipment.TransportationRequisitionLines.md#ParentLineNo) | int32 (nullable) | The number of the line within the parent document, which the current line executes. null when the current line does not execute another line. [Filter(eq)] 
| [VolumeCbm](Logistics.Shipment.TransportationRequisitionLines.md#VolumeCbm) | int32 (nullable) | The volume of the cargo, in CBM (cubic meters). null when it is unknown. 
| [WeightKg](Logistics.Shipment.TransportationRequisitionLines.md#WeightKg) | int32 (nullable) | The weight of the cargo, in KG (kilogramms). null when it is unknown. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CargoType](Logistics.Shipment.TransportationRequisitionLines.md#CargoType) | [Logistics.Shipment.CargoTypes](Logistics.Shipment.CargoTypes.md) | The type of the transported cargo. [Required] [Filter(multi eq)] |
| [ParentDocument](Logistics.Shipment.TransportationRequisitionLines.md#ParentDocument) | [General.Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] |
| [TransportationRequisition](Logistics.Shipment.TransportationRequisitionLines.md#TransportationRequisition) | [Logistics.Shipment.TransportationRequisitions](Logistics.Shipment.TransportationRequisitions.md) | The [TransportationRequisition](Logistics.Shipment.TransportationRequisitionLines.md#TransportationRequisition) to which this TransportationRequisitionLine belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ContentsDescription

> Textual description of the cargo contents. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LineNo

> Line number, unique within the TransportationRequisition. Usually is increasing number like 10, 20, 30, ... when initially entering the TransportationRequisition (in order to allow insertions with adjustment documents). [Required] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.TransportationRequisition.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.TransportationRequisition.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### PalletsCount

> Number of palettes comprising the cargo. null when it is unknown.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentLineNo

> The number of the line within the parent document, which the current line executes. null when the current line does not execute another line. [Filter(eq)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### VolumeCbm

> The volume of the cargo, in CBM (cubic meters). null when it is unknown.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### WeightKg

> The weight of the cargo, in KG (kilogramms). null when it is unknown.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CargoType

> The type of the transported cargo. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Shipment.CargoTypes](Logistics.Shipment.CargoTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ParentDocument

> The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TransportationRequisition

> The [TransportationRequisition](Logistics.Shipment.TransportationRequisitionLines.md#TransportationRequisition) to which this TransportationRequisitionLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Shipment.TransportationRequisitions](Logistics.Shipment.TransportationRequisitions.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Shipment.TransportationRequisitionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.TransportationRequisitionLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Shipment.TransportationRequisitionLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_TransportationRequisitionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_TransportationRequisitionLines?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Log_Transportation_Requisition_Lines?$top=10>

