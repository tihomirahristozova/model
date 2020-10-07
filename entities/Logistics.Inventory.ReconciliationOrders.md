# Logistics.Inventory.ReconciliationOrders

Obsolete. Not used. (Orders for store reconciliations. After an order is executed, store reconciliation is created). Entity: Inv_Reconciliation_Orders

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.ReconciliationOrders.md#Id) | guid |  
| [DueDate](Logistics.Inventory.ReconciliationOrders.md#DueDate) | datetime | Date, when the transaction is scheduled to occur. [Required] [Default(Today)] 
| [IsReleased](Logistics.Inventory.ReconciliationOrders.md#IsReleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Logistics.Inventory.ReconciliationOrders.md#IsSingleExecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Logistics.Inventory.ReconciliationOrders.md#Document) | [General.Documents](General.Documents.md) | The Id of the base document. [Required] [Filter(multi eq)] [Owner] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Lines | [Logistics.Inventory.ReconciliationOrderLines](Logistics.Inventory.ReconciliationOrderLines.md) | List of [ReconciliationOrderLine](Logistics.Inventory.ReconciliationOrderLines.md) child objects, based on the [Logistics.Inventory.ReconciliationOrderLine.ReconciliationOrder](Logistics.Inventory.ReconciliationOrderLines.md#ReconciliationOrder) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DueDate

> Date, when the transaction is scheduled to occur. [Required] [Default(Today)]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### IsReleased

> True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsSingleExecution

> Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### Document

> The Id of the base document. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.ReconciliationOrders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.ReconciliationOrders erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.ReconciliationOrders erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_ReconciliationOrders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_ReconciliationOrders?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Inv_Reconciliation_Orders?$top=10>

