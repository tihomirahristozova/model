---
uid: Logistics.Shipment.TransportationOrderLines
---
# Logistics.Shipment.TransportationOrderLines Entity

**Namespace:** [Logistics.Shipment](Logistics.Shipment.md)  

Different cargoes of a transportation order. Entity: Log_Transportation_Order_Lines

## Default Visualization
Default Display Text Format:  
_{LineNo} : {TransportationOrder.DocumentNo} {TransportationOrder.DocumentType.TypeName:T}_  
Default Search Member:  
_TransportationOrder.DocumentNo_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Shipment.TransportationOrders](Logistics.Shipment.TransportationOrders.md)  
Aggregate Root:  
[Logistics.Shipment.TransportationOrders](Logistics.Shipment.TransportationOrders.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ContentsDescription](Logistics.Shipment.TransportationOrderLines.md#contentsdescription) | string (128) | Textual description of the cargo contents. `Required` 
| [Id](Logistics.Shipment.TransportationOrderLines.md#id) | guid |  
| [LineNo](Logistics.Shipment.TransportationOrderLines.md#lineno) | int32 | Line number, unique within the TransportationOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the TransportationOrder (in order to allow insertions with adjustment documents). `Required` `Filter(eq)` 
| [Notes](Logistics.Shipment.TransportationOrderLines.md#notes) | string (max) __nullable__ | Notes for this TransportationOrderLine. `Introduced in version 18.2` 
| [PalletsCount](Logistics.Shipment.TransportationOrderLines.md#palletscount) | int32 __nullable__ | Number of palettes comprising the cargo. null when it is unknown. 
| [ParentLineNo](Logistics.Shipment.TransportationOrderLines.md#parentlineno) | int32 __nullable__ | The number of the line within the parent document, which the current line executes. null when the current line does not execute parent line. `Filter(eq)` 
| [VolumeCbm](Logistics.Shipment.TransportationOrderLines.md#volumecbm) | int32 __nullable__ | The volume of the cargo, in CBM (cubic meters). null when it is unknown. 
| [WeightKg](Logistics.Shipment.TransportationOrderLines.md#weightkg) | int32 __nullable__ | The weight of the cargo, in KG (kilogramms). null when it is unknown. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CargoType](Logistics.Shipment.TransportationOrderLines.md#cargotype) | [CargoTypes](Logistics.Shipment.CargoTypes.md) | The type of the transported cargo. `Required` `Filter(multi eq)` |
| [Document](Logistics.Shipment.TransportationOrderLines.md#document) | [TransportationOrders](Logistics.Shipment.TransportationOrders.md) | The `TransportationOrder`(Logistics.Shipment.TransportationOrderLines.md#transportationorder) to which this TransportationOrderLine belongs. `Required` `Filter(multi eq)` |
| [ParentDocument](Logistics.Shipment.TransportationOrderLines.md#parentdocument) | [Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. `Filter(multi eq)` |
| [TransportationOrder](Logistics.Shipment.TransportationOrderLines.md#transportationorder) | [TransportationOrders](Logistics.Shipment.TransportationOrders.md) | The `TransportationOrder`(Logistics.Shipment.TransportationOrderLines.md#transportationorder) to which this TransportationOrderLine belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### ContentsDescription

Textual description of the cargo contents. `Required`

_Type_: **string (128)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Line number, unique within the TransportationOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the TransportationOrder (in order to allow insertions with adjustment documents). `Required` `Filter(eq)`

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.TransportationOrder.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.TransportationOrder.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this TransportationOrderLine. `Introduced in version 18.2`

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### PalletsCount

Number of palettes comprising the cargo. null when it is unknown.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentLineNo

The number of the line within the parent document, which the current line executes. null when the current line does not execute parent line. `Filter(eq)`

_Type_: **int32 __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### VolumeCbm

The volume of the cargo, in CBM (cubic meters). null when it is unknown.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### WeightKg

The weight of the cargo, in KG (kilogramms). null when it is unknown.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CargoType

The type of the transported cargo. `Required` `Filter(multi eq)`

_Type_: **[CargoTypes](Logistics.Shipment.CargoTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Document

The `TransportationOrder`(Logistics.Shipment.TransportationOrderLines.md#transportationorder) to which this TransportationOrderLine belongs. `Required` `Filter(multi eq)`

_Type_: **[TransportationOrders](Logistics.Shipment.TransportationOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ParentDocument

The document, which the current line executes. null when the current line does not execute another line. `Filter(multi eq)`

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportationOrder

The `TransportationOrder`(Logistics.Shipment.TransportationOrderLines.md#transportationorder) to which this TransportationOrderLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[TransportationOrders](Logistics.Shipment.TransportationOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Logistics.Shipment.TransportationOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Shipment.TransportationOrderLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_TransportationOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_TransportationOrderLines?$top=10>

