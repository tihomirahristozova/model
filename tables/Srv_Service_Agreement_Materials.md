# Table Srv_Service_Agreement_Materials

Contains the free materials, included in the service agreement. Entity: Srv_Service_Agreement_Materials

## Owner Tables Hierarchy

* [Srv_Service_Agreements](Srv_Service_Agreements.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc.|
|[Product_Id](#product_id)|`uniqueidentifier` |Paid or agreed in advance material that won't be invoiced after service activities|
|[Quantity](#quantity)|`decimal(18, 3)` |Quantity of the agreed material|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Start_Date](#start_date)|`datetime` |Start date from which the agreedment for the material is valid. For the agreement period, the material could be used free of charge in service activities.|
|[End_Date](#end_date)|`datetime` |End date to which the agreedment for the material is valid. For the agreement period, the material could be used free of charge in service activities.|
|[Service_Agreement_Material_Id](#service_agreement_material_id)|`uniqueidentifier` `PK`||
|[Service_Agreement_Id](#service_agreement_id)|`uniqueidentifier` ||
|[Quantity_Base](#quantity_base)|`decimal(18, 3)` Readonly|The equivalence of Quantity in the base measurement category of the product.|
|[Row_Version](#row_version)|`timestamp` ||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### End_Date

| Property | Value |
| - | - |
|Type|datetime|

### Service_Agreement_Material_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Agreement_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|


