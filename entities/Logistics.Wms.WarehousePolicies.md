---
uid: Logistics.Wms.WarehousePolicies
---
# Logistics.Wms.WarehousePolicies Entity

**Namespace:** [Logistics.Wms](Logistics.Wms.md)  

Warehouse Policies is a hierarchical system for applying policies to warehouse operations. Entity: Wms_Warehouse_Policies (Introduced in version 22.1.4.23)

## Default Visualization
Default Display Text Format:  
_{Warehouse.Name:T}_  
Default Search Members:  
_Warehouse.Name_  
Name Data Member:  
_Warehouse.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md)  
Aggregate Root:  
[Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](Logistics.Wms.WarehousePolicies.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [FromDate](Logistics.Wms.WarehousePolicies.md#fromdate) | date __nullable__ | When set, specifies the activation date of the policy. `Filter(eq;ge;le)` 
| [Id](Logistics.Wms.WarehousePolicies.md#id) | guid |  
| [Importance](Logistics.Wms.WarehousePolicies.md#importance) | int32 | The importance of the policy, relative to other applicable policies. Higher numbers indicate higher importance. `Required` `Default(0)` `Filter(eq;ge;le)` 
| [Note](Logistics.Wms.WarehousePolicies.md#note) | string (max) __nullable__ |  
| [ObjectVersion](Logistics.Wms.WarehousePolicies.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [PolicyKind](Logistics.Wms.WarehousePolicies.md#policykind) | [PolicyKind](Logistics.Wms.WarehousePolicies.md#policykind) | The kind of policy, which is being applied. `Required` `Filter(multi eq)` 
| [ToDate](Logistics.Wms.WarehousePolicies.md#todate) | date __nullable__ | When set, specifies the de-activation date of the policy. `Filter(eq;ge;le)` 
| [Value](Logistics.Wms.WarehousePolicies.md#value) | string (64) | The value specified for the policy. For boolean policies, allowed values are "true" and "false". `Required` `Filter(eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Product](Logistics.Wms.WarehousePolicies.md#product) | [Products](General.Products.Products.md) (nullable) | When set, specifies that the policy will apply to the specified product only. `Filter(multi eq)` |
| [ProductGroup](Logistics.Wms.WarehousePolicies.md#productgroup) | [ProductGroups](General.Products.ProductGroups.md) (nullable) | When set, specifies that the policy will apply to the specified product group only. `Filter(multi eq)` `Introduced in version 22.1.4.36` |
| [ProductType](Logistics.Wms.WarehousePolicies.md#producttype) | [ProductTypes](General.Products.ProductTypes.md) (nullable) | When set, specifies that the policy will apply to the specified product type only. `Filter(multi eq)` |
| [Warehouse](Logistics.Wms.WarehousePolicies.md#warehouse) | [Warehouses](Logistics.Wms.Warehouses.md) | The warehouse for which the policy is defined. . `Required` `Filter(multi eq)` `ReadOnly` `Owner` |
| [Zone](Logistics.Wms.WarehousePolicies.md#zone) | [WarehouseZones](Logistics.Wms.WarehouseZones.md) (nullable) | When set, specifies that the policy will apply to the specified zone and its sub-zones. `Filter(multi eq)` |


## Attribute Details

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### FromDate

When set, specifies the activation date of the policy. `Filter(eq;ge;le)`

_Type_: **date __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Importance

The importance of the policy, relative to other applicable policies. Higher numbers indicate higher importance. `Required` `Default(0)` `Filter(eq;ge;le)`

_Type_: **int32**  
_Category_: **System**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Note

_Type_: **string (max) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### PolicyKind

The kind of policy, which is being applied. `Required` `Filter(multi eq)`

_Type_: **[PolicyKind](Logistics.Wms.WarehousePolicies.md#policykind)**  
_Category_: **System**  
Allowed values for the `PolicyKind`(Logistics.Wms.WarehousePolicies.md#policykind) data attribute  
_Allowed Values (Logistics.Wms.WarehousePoliciesRepository.PolicyKind Enum Members)_  

| Value | Description |
| ---- | --- |
| AllowProductChange | Allow executing with а different product than the ordered.. Stored as 'APC'. <br /> _Database Value:_ 'APC' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AllowProductChange' |
| AllowLotChange | Allow executing with a different lot than the ordered.. Stored as 'ATC'. <br /> _Database Value:_ 'ATC' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'AllowLotChange' |
| AllowLocationChange | Allow executing from a different location than the ordered.. Stored as 'ALC'. <br /> _Database Value:_ 'ALC' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'AllowLocationChange' |
| AllowUnitChange | Allow executing of a quantity in a different measurement unit than the ordered.. Stored as 'AUC'. <br /> _Database Value:_ 'AUC' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'AllowUnitChange' |
| RequireSourceScan | Require scanning of the source location when moving/dispatching. Stored as 'RSS'. <br /> _Database Value:_ 'RSS' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'RequireSourceScan' |
| RequireDestinationScan | Require scanning of the destination location when moving/receiving. Stored as 'RDS'. <br /> _Database Value:_ 'RDS' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'RequireDestinationScan' |
| AllowLineSkip | Allow skipping of an order line when executing (allow quantity = 0). Stored as 'ALS'. <br /> _Database Value:_ 'ALS' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'AllowLineSkip' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ToDate

When set, specifies the de-activation date of the policy. `Filter(eq;ge;le)`

_Type_: **date __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Value

The value specified for the policy. For boolean policies, allowed values are "true" and "false". `Required` `Filter(eq;ge;le)`

_Type_: **string (64)**  
_Category_: **System**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  


## Reference Details

### Product

When set, specifies that the policy will apply to the specified product only. `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md) (nullable)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductGroup

When set, specifies that the policy will apply to the specified product group only. `Filter(multi eq)` `Introduced in version 22.1.4.36`

_Type_: **[ProductGroups](General.Products.ProductGroups.md) (nullable)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductType

When set, specifies that the policy will apply to the specified product type only. `Filter(multi eq)`

_Type_: **[ProductTypes](General.Products.ProductTypes.md) (nullable)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### Warehouse

The warehouse for which the policy is defined. . `Required` `Filter(multi eq)` `ReadOnly` `Owner`

_Type_: **[Warehouses](Logistics.Wms.Warehouses.md)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Zone

When set, specifies that the policy will apply to the specified zone and its sub-zones. `Filter(multi eq)`

_Type_: **[WarehouseZones](Logistics.Wms.WarehouseZones.md) (nullable)**  
_Category_: **System**  
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

[!list limit=1000 erp.entity=Logistics.Wms.WarehousePolicies erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Wms.WarehousePolicies erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehousePolicies?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehousePolicies?$top=10>

