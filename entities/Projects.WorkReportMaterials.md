---
uid: Projects.WorkReportMaterials
---
# Projects.WorkReportMaterials Entity

Each record contains a consumed material, reported by the related Work Report. Entity: Prj_Work_Report_Materials

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Projects.WorkReportMaterials.md#id) | guid |  
| [Quantity](Projects.WorkReportMaterials.md#quantity) | decimal | The consumed quantity of the material. [Required] [Default(0)] [Filter(eq;like)] 
| [QuantityBase](Projects.WorkReportMaterials.md#quantitybase) | decimal | The equivalence of Quantity in the base measurement unit of the Material. [Required] [Default(0)] [Filter(eq;like)] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaterialProduct](Projects.WorkReportMaterials.md#materialproduct) | [Products](General.Products.Products.md) | The consumed material. [Required] [Filter(multi eq)] |
| [ProjectTask](Projects.WorkReportMaterials.md#projecttask) | [ProjectTasks](Projects.ProjectTasks.md) | The project task for which the materials are reported. [Required] [Filter(multi eq)] |
| [QuantityUnit](Projects.WorkReportMaterials.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. It is strongly suggested that the same unit is used for planning and usage reporting. [Required] [Filter(multi eq)] |
| [WorkReport](Projects.WorkReportMaterials.md#workreport) | [WorkReports](Projects.WorkReports.md) | The [WorkReport](Projects.WorkReportMaterials.md#workreport) to which this WorkReportMaterial belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Quantity

The consumed quantity of the material. [Required] [Default(0)] [Filter(eq;like)]

_Type_: **decimal**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### QuantityBase

The equivalence of Quantity in the base measurement unit of the Material. [Required] [Default(0)] [Filter(eq;like)] [ReadOnly]

_Type_: **decimal**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`IIF( ( ( obj.QuantityUnit != null) AndAlso ( obj.MaterialProduct != null)), new Quantity( obj.Quantity, obj.QuantityUnit).ConvertTo( obj.MaterialProduct.BaseUnit, obj.MaterialProduct).Value, obj.QuantityBase)`

## Reference Details

### MaterialProduct

The consumed material. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProjectTask

The project task for which the materials are reported. [Required] [Filter(multi eq)]

_Type_: **[ProjectTasks](Projects.ProjectTasks.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.WorkReport.ProjectTask`

_Front-End Recalc Expressions:_  
`obj.WorkReport.ProjectTask`
### QuantityUnit

The measurement unit of Quantity. It is strongly suggested that the same unit is used for planning and usage reporting. [Required] [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WorkReport

The [WorkReport](Projects.WorkReportMaterials.md#workreport) to which this WorkReportMaterial belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[WorkReports](Projects.WorkReports.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Projects.WorkReportMaterials erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.WorkReportMaterials erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_WorkReportMaterials?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_WorkReportMaterials?$top=10>

