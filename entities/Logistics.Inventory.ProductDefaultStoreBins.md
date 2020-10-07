# Logistics.Inventory.ProductDefaultStoreBins

The default store bins in which products should be placed. Entity: Inv_Product_Default_Store_Bins

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.ProductDefaultStoreBins.md#Id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultBin](Logistics.Inventory.ProductDefaultStoreBins.md#DefaultBin) | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) | The default bin, which should be used for this product. [Required] [Filter(multi eq)] |
| [Product](Logistics.Inventory.ProductDefaultStoreBins.md#Product) | [General.Products.Products](General.Products.Products.md) | The [Product](General.Products.Products.md) to which this ProductDefaultStoreBin belongs. [Required] [Filter(multi eq)] [Owner] |
| [Store](Logistics.Inventory.ProductDefaultStoreBins.md#Store) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) | The store, for which the default bin is specified. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  


## Reference Details

### DefaultBin

> The default bin, which should be used for this product. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The [Product](General.Products.Products.md) to which this ProductDefaultStoreBin belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Store

> The store, for which the default bin is specified. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.ProductDefaultStoreBins erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.ProductDefaultStoreBins erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.ProductDefaultStoreBins erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_ProductDefaultStoreBins?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_ProductDefaultStoreBins?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Inv_Product_Default_Store_Bins?$top=10>

