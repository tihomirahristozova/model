---
uid: Logistics.Inventory.SerialNumbers
---
# Logistics.Inventory.SerialNumbers

Serial numbers, used by the items. Rows are created on first occurrence of the serial number in a document. Rows can be deleted after deleting the last occurence of the serial number in a document. Entity: Inv_Serial_Numbers

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.SerialNumbers.md#id) | guid |  
| [SerialNumberField](Logistics.Inventory.SerialNumbers.md#serialnumberfield) | string | The serial number text. [Required] [Filter(multi eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Product](Logistics.Inventory.SerialNumbers.md#product) | [Products](General.Products.Products.md) | The product, to which the serial number is bound. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### SerialNumberField

> The serial number text. [Required] [Filter(multi eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### Product

> The product, to which the serial number is bound. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Inventory.SerialNumbers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.SerialNumbers erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.SerialNumbers erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_SerialNumbers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_SerialNumbers?$top=10>

