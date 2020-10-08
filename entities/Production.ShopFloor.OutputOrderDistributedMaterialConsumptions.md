---
uid: Production.ShopFloor.OutputOrderDistributedMaterialConsumptions
---
# Production.ShopFloor.OutputOrderDistributedMaterialConsumptions

Contains the quantity of materials distributed over the output order lines. Entity: Prd_Output_Order_Distributed_Material_Consumptions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ConsumedCost](Production.ShopFloor.OutputOrderDistributedMaterialConsumptions.md#consumedcost) | [Amount](../data-types.md#amount) | Cost of the actually issued Consumed_Quantity. [Currency: ConsumptionOrderLine.GetIssueCurrency()] [Required] [Default(0)] [ReadOnly] 
| [ConsumedQuantity](Production.ShopFloor.OutputOrderDistributedMaterialConsumptions.md#consumedquantity) | [Quantity](../data-types.md#quantity) | Part of the quantity in the consumption order line which was used for the product in the output order line. [Unit: ConsumptionOrderLine.ConsumedQuantityUnit] [Required] [Default(0)] [ReadOnly] 
| [Id](Production.ShopFloor.OutputOrderDistributedMaterialConsumptions.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ConsumptionOrderLine](Production.ShopFloor.OutputOrderDistributedMaterialConsumptions.md#consumptionorderline) | [Production.ShopFloor.ConsumptionOrderLines](Production.ShopFloor.ConsumptionOrderLines.md) | Consumption order line which requested the Consumed_Quantity. [Required] [Filter(multi eq)] [ReadOnly] |
| [OutputOrderLine](Production.ShopFloor.OutputOrderDistributedMaterialConsumptions.md#outputorderline) | [Production.ShopFloor.OutputOrderLines](Production.ShopFloor.OutputOrderLines.md) | The output order line for which the distribution is recorded. [Required] [Filter(multi eq)] [ReadOnly] [Owner] |


## Attribute Details

### ConsumedCost

> Cost of the actually issued Consumed_Quantity. [Currency: ConsumptionOrderLine.GetIssueCurrency()] [Required] [Default(0)] [ReadOnly]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ConsumedQuantity

> Part of the quantity in the consumption order line which was used for the product in the output order line. [Unit: ConsumptionOrderLine.ConsumedQuantityUnit] [Required] [Default(0)] [ReadOnly]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### ConsumptionOrderLine

> Consumption order line which requested the Consumed_Quantity. [Required] [Filter(multi eq)] [ReadOnly]

_Type_: **[Production.ShopFloor.ConsumptionOrderLines](Production.ShopFloor.ConsumptionOrderLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### OutputOrderLine

> The output order line for which the distribution is recorded. [Required] [Filter(multi eq)] [ReadOnly] [Owner]

_Type_: **[Production.ShopFloor.OutputOrderLines](Production.ShopFloor.OutputOrderLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Production.ShopFloor.OutputOrderDistributedMaterialConsumptions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.ShopFloor.OutputOrderDistributedMaterialConsumptions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.ShopFloor.OutputOrderDistributedMaterialConsumptions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_ShopFloor_OutputOrderDistributedMaterialConsumptions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_ShopFloor_OutputOrderDistributedMaterialConsumptions?$top=10>

