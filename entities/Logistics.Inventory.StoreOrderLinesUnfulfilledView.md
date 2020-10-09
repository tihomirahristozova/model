---
uid: Logistics.Inventory.StoreOrderLinesUnfulfilledView
---
# Logistics.Inventory.StoreOrderLinesUnfulfilledView Entity

Returns the remaining (unfulfilled) quantity and cost for each Store Order Line in Store Orders, which are Planned, FirmPlanned or Released. Is_Fulfilled and Is_QuantityFulfilled can be used to filter out lines which appear fulfilled. For best performance, the store orders should be finished after fulfilling. Entity: Inv_Store_Order_Lines_Unfulfilled_View

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentDate](Logistics.Inventory.StoreOrderLinesUnfulfilledView.md#documentdate) | datetime | The date on which the document was issued. [Required] [Default(Today)] [Filter(eq;ge;le)] 
| [IsFulfilled](Logistics.Inventory.StoreOrderLinesUnfulfilledView.md#isfulfilled) | int32 | Returns 1/true when both the Quantity and Cost are fulfilled or only negligible (less than 0.001 for qty and 0.01 for cost) sums remain. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling. [Required] [Filter(multi eq)] 
| [IsQuantityFulfilled](Logistics.Inventory.StoreOrderLinesUnfulfilledView.md#isquantityfulfilled) | int32 | Returns 1/true when the Quantity is fulfilled or only negligible (less than 0.001) sum remains. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling. [Required] [Filter(multi eq)] 
| [OrderRemainingLineCost](Logistics.Inventory.StoreOrderLinesUnfulfilledView.md#orderremaininglinecost) | decimal | The remaining (unfulfilled) line cost of the order line. [Required] [Filter(multi eq;ge;le)] 
| [OrderRemainingQuantityBase](Logistics.Inventory.StoreOrderLinesUnfulfilledView.md#orderremainingquantitybase) | decimal | The remaining (unfulfilled) quantity of the order line in base measurement unit. [Required] [Filter(multi eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Logistics.Inventory.StoreOrderLinesUnfulfilledView.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document. [Required] [Filter(multi eq)] |
| [Lot](Logistics.Inventory.StoreOrderLinesUnfulfilledView.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | If non-null, contains the specific lot to use for the movement. [Filter(multi eq)] |
| [Product](Logistics.Inventory.StoreOrderLinesUnfulfilledView.md#product) | [Products](General.Products.Products.md) | The product which should be received/issued. [Required] [Filter(multi eq)] |
| [ProductVariant](Logistics.Inventory.StoreOrderLinesUnfulfilledView.md#productvariant) | [ProductVariants](General.ProductVariants.md) (nullable) | If specified determines which product variant of the current product in this line is used. [Filter(multi eq)] |
| [SerialNumber](Logistics.Inventory.StoreOrderLinesUnfulfilledView.md#serialnumber) | [SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)] |
| [Store](Logistics.Inventory.StoreOrderLinesUnfulfilledView.md#store) | [Stores](Logistics.Inventory.Stores.md) | The designated warehouse for the operation. [Required] [Filter(multi eq)] |
| [StoreOrderLine](Logistics.Inventory.StoreOrderLinesUnfulfilledView.md#storeorderline) | [StoreOrderLines](Logistics.Inventory.StoreOrderLines.md) | Store order line Id. [Required] [Default(New Guid)] [Filter(multi eq)] |


## Attribute Details

### DocumentDate

The date on which the document was issued. [Required] [Default(Today)] [Filter(eq;ge;le)]

_Type_: **datetime**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### IsFulfilled

Returns 1/true when both the Quantity and Cost are fulfilled or only negligible (less than 0.001 for qty and 0.01 for cost) sums remain. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling. [Required] [Filter(multi eq)]

_Type_: **int32**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### IsQuantityFulfilled

Returns 1/true when the Quantity is fulfilled or only negligible (less than 0.001) sum remains. Please note, that filtering by this fields forces full scan and calculation of remaining amounts for all non-finished store orders. For best performance, the store orders should be finished after fulfilling. [Required] [Filter(multi eq)]

_Type_: **int32**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### OrderRemainingLineCost

The remaining (unfulfilled) line cost of the order line. [Required] [Filter(multi eq;ge;le)]

_Type_: **decimal**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

### OrderRemainingQuantityBase

The remaining (unfulfilled) quantity of the order line in base measurement unit. [Required] [Filter(multi eq;ge;le)]

_Type_: **decimal**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

The enterprise company which issued the document. [Required] [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

If non-null, contains the specific lot to use for the movement. [Filter(multi eq)]

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The product which should be received/issued. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductVariant

If specified determines which product variant of the current product in this line is used. [Filter(multi eq)]

_Type_: **[ProductVariants](General.ProductVariants.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### SerialNumber

Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)]

_Type_: **[SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

The designated warehouse for the operation. [Required] [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### StoreOrderLine

Store order line Id. [Required] [Default(New Guid)] [Filter(multi eq)]

_Type_: **[StoreOrderLines](Logistics.Inventory.StoreOrderLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  



## Business Rules

[!list erp.entity=Logistics.Inventory.StoreOrderLinesUnfulfilledView erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.StoreOrderLinesUnfulfilledView erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.StoreOrderLinesUnfulfilledView erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_StoreOrderLinesUnfulfilledView?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_StoreOrderLinesUnfulfilledView?$top=10>

