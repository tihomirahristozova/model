---
uid: Projects.ProjectTaskMaterials
---
# Projects.ProjectTaskMaterials Entity

**Namespace:** [Projects](Projects.md)  

Contains the materials, which are required for a project task. Entity: Prj_Project_Task_Materials

## Default Visualization
Default Display Text Format:  
_{ProjectTask.TaskName}_  
Default Search Members:  
_ProjectTask.TaskName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Projects.ProjectTasks](Projects.ProjectTasks.md)  
Aggregate Root:  
[Projects.ProjectTasks](Projects.ProjectTasks.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BudgetedMaterialAmount](Projects.ProjectTaskMaterials.md#budgetedmaterialamount) | [Amount (12, 2)](../data-types.md#amount) __nullable__ | Budgeted amount for the material in the currency of the project. null means there is still no budgeted amount. `Currency: ProjectTask.Project.BudgetingCurrency` 
| [Id](Projects.ProjectTaskMaterials.md#id) | guid |  
| [LineNumber](Projects.ProjectTaskMaterials.md#linenumber) | int32 | Line number within the task, increased in steps of 10. Used for sorting purposes. `Required` `Default(0)` 
| [ObjectVersion](Projects.ProjectTaskMaterials.md#objectversion) | int32 |  
| [Quantity](Projects.ProjectTaskMaterials.md#quantity) | [Quantity (9, 3)](../data-types.md#quantity) | The required quantity of the material. `Unit: QuantityUnit` `Required` `Default(1)` 
| [QuantityBase](Projects.ProjectTaskMaterials.md#quantitybase) | decimal (9, 3) | The equivalence of Quantity in the base measurement unit of the Material. `Required` `Default(0)` `ReadOnly` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaterialProduct](Projects.ProjectTaskMaterials.md#materialproduct) | [Products](General.Products.Products.md) | The product Id of the required material. `Required` `Filter(multi eq)` |
| [ProjectTask](Projects.ProjectTaskMaterials.md#projecttask) | [ProjectTasks](Projects.ProjectTasks.md) | The task for which is the material requirement. `Required` `Filter(multi eq)` `Owner` |
| [QuantityUnit](Projects.ProjectTaskMaterials.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of the required quantity. `Required` `Filter(multi eq)` |


## Attribute Details

### BudgetedMaterialAmount

Budgeted amount for the material in the currency of the project. null means there is still no budgeted amount. `Currency: ProjectTask.Project.BudgetingCurrency`

_Type_: **[Amount (12, 2)](../data-types.md#amount) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.MaterialProduct != null), obj.CalculateBudgetMaterialAmount( obj.Quantity), new Amount( 0, obj.ProjectTask.Project.BudgetingCurrency))`
### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNumber

Line number within the task, increased in steps of 10. Used for sorting purposes. `Required` `Default(0)`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Back-End Default Expression:_  
`( obj.ProjectTask.Materials.Select( c => c.LineNumber).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.ProjectTask.Materials.Select( c => c.LineNumber).DefaultIfEmpty( 0).Max( ) + 10)`
### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Quantity

The required quantity of the material. `Unit: QuantityUnit` `Required` `Default(1)`

_Type_: **[Quantity (9, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

The equivalence of Quantity in the base measurement unit of the Material. `Required` `Default(0)` `ReadOnly`

_Type_: **decimal (9, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`IIF( ( ( obj.QuantityUnit != null) AndAlso ( obj.MaterialProduct != null)), obj.Quantity.ConvertTo( obj.MaterialProduct.BaseUnit, obj.MaterialProduct).Value, obj.QuantityBase)`

## Reference Details

### MaterialProduct

The product Id of the required material. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProjectTask

The task for which is the material requirement. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ProjectTasks](Projects.ProjectTasks.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### QuantityUnit

The measurement unit of the required quantity. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Projects.ProjectTaskMaterials erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Projects.ProjectTaskMaterials erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectTaskMaterials?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectTaskMaterials?$top=10>

