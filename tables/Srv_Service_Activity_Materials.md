# Table Srv_Service_Activity_Materials

Contains the materials, which were actually used during the service activity (repair). Entity: Srv_Service_Activity_Materials

## Owner Tables Hierarchy

* [Srv_Service_Activities](Srv_Service_Activities.md)
* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc.|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which was used as material.|
|[Quantity](#quantity)|`decimal(18, 3)` |Quantity of the product, that was used|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity. Initially is set to the default unit for the product|
|[Line_Store_Id](#line_store_id)|`uniqueidentifier` |The store from which the product was taken. NULL = use the store from the header|
|[Service_Activity_Material_Id](#service_activity_material_id)|`uniqueidentifier` `PK`||
|[Service_Activity_Id](#service_activity_id)|`uniqueidentifier` ||
|[Service_Object_Id](#service_object_id)|`uniqueidentifier` |The service object for which the material is used. NULL means unkown object or N/A|
|[Covered_By_Guarantee](#covered_by_guarantee)|`bit` |True when the used material is covered by the guarantee.|
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

### Line_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Activity_Material_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Covered_By_Guarantee

| Property | Value |
| - | - |
|Type|bit|

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


