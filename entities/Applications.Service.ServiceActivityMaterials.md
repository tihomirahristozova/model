---
uid: Applications.Service.ServiceActivityMaterials
---
# Applications.Service.ServiceActivityMaterials Entity

Contains the materials, which were actually used during the service activity (repair). Entity: Srv_Service_Activity_Materials

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CoveredByGuarantee](Applications.Service.ServiceActivityMaterials.md#coveredbyguarantee) | boolean | True when the used material is covered by the guarantee. [Required] [Default(false)] 
| [Id](Applications.Service.ServiceActivityMaterials.md#id) | guid |  
| [LineNo](Applications.Service.ServiceActivityMaterials.md#lineno) | int32 | Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required] 
| [Quantity](Applications.Service.ServiceActivityMaterials.md#quantity) | [Quantity](../data-types.md#quantity) | Quantity of the product, that was used. [Unit: QuantityUnit] [Required] 
| [QuantityBase](Applications.Service.ServiceActivityMaterials.md#quantitybase) | [Quantity](../data-types.md#quantity) | The equivalence of Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] 
| [StandardQuantityBase](Applications.Service.ServiceActivityMaterials.md#standardquantitybase) | [Quantity](../data-types.md#quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [LineStore](Applications.Service.ServiceActivityMaterials.md#linestore) | [Stores](Logistics.Inventory.Stores.md) (nullable) | The store from which the product was taken. null = use the store from the header. [Filter(multi eq)] |
| [Product](Applications.Service.ServiceActivityMaterials.md#product) | [Products](General.Products.Products.md) | The product, which was used as material. [Required] [Filter(multi eq)] |
| [QuantityUnit](Applications.Service.ServiceActivityMaterials.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. Initially is set to the default unit for the product. [Required] [Filter(multi eq)] |
| [ServiceActivity](Applications.Service.ServiceActivityMaterials.md#serviceactivity) | [ServiceActivities](Applications.Service.ServiceActivities.md) | The [ServiceActivity](Applications.Service.ServiceActivityMaterials.md#serviceactivity) to which this ServiceActivityMaterial belongs. [Required] [Filter(multi eq)] [Owner] |
| [ServiceObject](Applications.Service.ServiceActivityMaterials.md#serviceobject) | [ServiceObjects](Applications.Service.ServiceObjects.md) (nullable) | The service object for which the material is used. null means unkown object or N/A. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| ServiceActivity<br />AgreedMaterials | [ServiceActivityAgreedMaterials](Applications.Service.ServiceActivityAgreedMaterials.md) | List of [ServiceActivity<br />AgreedMaterial](Applications.Service.ServiceActivity<br />AgreedMaterials.md) child objects, based on the [Applications.Service.ServiceActivity<br />AgreedMaterial.ServiceActivityMaterial](Applications.Service.ServiceActivity<br />AgreedMaterials.md#serviceactivitymaterial) back  


## Attribute Details

### CoveredByGuarantee

True when the used material is covered by the guarantee. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.ServiceActivity.Materials.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.ServiceActivity.Materials.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Quantity

Quantity of the product, that was used. [Unit: QuantityUnit] [Required]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### QuantityBase

The equivalence of Quantity in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### StandardQuantityBase

The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2)

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

## Reference Details

### LineStore

The store from which the product was taken. null = use the store from the header. [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.ServiceActivity.Store`

_Front-End Recalc Expressions:_  
`obj.ServiceActivity.Store`
### Product

The product, which was used as material. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

The measurement unit of Quantity. Initially is set to the default unit for the product. [Required] [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Product.BaseUnit`
### ServiceActivity

The [ServiceActivity](Applications.Service.ServiceActivityMaterials.md#serviceactivity) to which this ServiceActivityMaterial belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[ServiceActivities](Applications.Service.ServiceActivities.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ServiceObject

The service object for which the material is used. null means unkown object or N/A. [Filter(multi eq)]

_Type_: **[ServiceObjects](Applications.Service.ServiceObjects.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.ServiceActivity.DefaultServiceObject`

_Front-End Recalc Expressions:_  
`obj.ServiceActivity.DefaultServiceObject`


## Business Rules

[!list erp.entity=Applications.Service.ServiceActivityMaterials erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Service.ServiceActivityMaterials erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Service_ServiceActivityMaterials?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Service_ServiceActivityMaterials?$top=10>

