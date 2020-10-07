# Applications.Service.ServiceActivityMaterials

Contains the materials, which were actually used during the service activity (repair). Entity: Srv_Service_Activity_Materials

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Service.ServiceActivityMaterials.md#Id) | guid |  
| [CoveredByGuarantee](Applications.Service.ServiceActivityMaterials.md#CoveredByGuarantee) | boolean | True when the used material is covered by the guarantee. [Required] [Default(false)] 
| [LineNo](Applications.Service.ServiceActivityMaterials.md#LineNo) | int32 | Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required] 
| [Quantity](Applications.Service.ServiceActivityMaterials.md#Quantity) | [Quantity](../data-types/Quantity.md) | Quantity of the product, that was used. [Unit: QuantityUnit] [Required] 
| [QuantityBase](Applications.Service.ServiceActivityMaterials.md#QuantityBase) | [Quantity](../data-types/Quantity.md) | The equivalence of Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] 
| [StandardQuantityBase](Applications.Service.ServiceActivityMaterials.md#StandardQuantityBase) | [Quantity](../data-types/Quantity.md) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [LineStore](Applications.Service.ServiceActivityMaterials.md#LineStore) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | The store from which the product was taken. null = use the store from the header. [Filter(multi eq)] |
| [Product](Applications.Service.ServiceActivityMaterials.md#Product) | [General.Products.Products](General.Products.Products.md) | The product, which was used as material. [Required] [Filter(multi eq)] |
| [QuantityUnit](Applications.Service.ServiceActivityMaterials.md#QuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. Initially is set to the default unit for the product. [Required] [Filter(multi eq)] |
| [ServiceActivity](Applications.Service.ServiceActivityMaterials.md#ServiceActivity) | [Applications.Service.ServiceActivities](Applications.Service.ServiceActivities.md) | The [ServiceActivity](Applications.Service.ServiceActivityMaterials.md#ServiceActivity) to which this ServiceActivityMaterial belongs. [Required] [Filter(multi eq)] [Owner] |
| [ServiceObject](Applications.Service.ServiceActivityMaterials.md#ServiceObject) | [Applications.Service.ServiceObjects](Applications.Service.ServiceObjects.md) (nullable) | The service object for which the material is used. null means unkown object or N/A. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| ServiceActivityAgreedMaterials | [Applications.Service.ServiceActivityAgreedMaterials](Applications.Service.ServiceActivityAgreedMaterials.md) | List of [ServiceActivityAgreedMaterial](Applications.Service.ServiceActivityAgreedMaterials.md) child objects, based on the [Applications.Service.ServiceActivityAgreedMaterial.ServiceActivityMaterial](Applications.Service.ServiceActivityAgreedMaterials.md#ServiceActivityMaterial) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CoveredByGuarantee

> True when the used material is covered by the guarantee. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LineNo

> Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.ServiceActivity.Materials.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.ServiceActivity.Materials.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### Quantity

> Quantity of the product, that was used. [Unit: QuantityUnit] [Required]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### QuantityBase

> The equivalence of Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### StandardQuantityBase

> The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0)

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

## Reference Details

### LineStore

> The store from which the product was taken. null = use the store from the header. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.ServiceActivity.Store`

_Front-End Recalc Expressions:_  
`obj.ServiceActivity.Store`
### Product

> The product, which was used as material. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### QuantityUnit

> The measurement unit of Quantity. Initially is set to the default unit for the product. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Product.BaseUnit`
### ServiceActivity

> The [ServiceActivity](Applications.Service.ServiceActivityMaterials.md#ServiceActivity) to which this ServiceActivityMaterial belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Service.ServiceActivities](Applications.Service.ServiceActivities.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ServiceObject

> The service object for which the material is used. null means unkown object or N/A. [Filter(multi eq)]

_Type_: **[Applications.Service.ServiceObjects](Applications.Service.ServiceObjects.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.ServiceActivity.DefaultServiceObject`

_Front-End Recalc Expressions:_  
`obj.ServiceActivity.DefaultServiceObject`


## Business Rules

[!list erp.entity=Applications.Service.ServiceActivityMaterials erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceActivityMaterials erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Service.ServiceActivityMaterials erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceActivityMaterials?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceActivityMaterials?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Srv_Service_Activity_Materials?$top=10>

