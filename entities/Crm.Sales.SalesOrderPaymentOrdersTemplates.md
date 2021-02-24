---
uid: Crm.Sales.SalesOrderPaymentOrdersTemplates
---
# Crm.Sales.SalesOrderPaymentOrdersTemplates Entity

**Namespace:** [Crm.Sales](Crm.Sales.md)  

Contains options for generation of payment orders. Each option set is assigned to specific generation route. Entity: Crm_Sales_Order_Payment_Orders_Templates

## Default Visualization
Default Display Text Format:  
_{Route.ProcedureName:T}_  
Default Search Member:  
_Route.ProcedureName_  

## Aggregate
  @aggregates  
Aggregate Parent:  
[Systems.Workflow.Routes](Systems.Workflow.Routes.md)  
Aggregate Root:  
[General.DocumentTypes](General.DocumentTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreateForInvoicedAmounts](Crm.Sales.SalesOrderPaymentOrdersTemplates.md#createforinvoicedamounts) | boolean | True to add to the payment order, the part of the amount of the sales order, which is invoiced. [Required] 
| [CreateForNotInvoiced<br />Amounts](Crm.Sales.SalesOrderPaymentOrdersTemplates.md#createfornotinvoicedamounts) | boolean | True to add to the payment order, the part of the amount of the sales order, which is not included in any invoice. [Required] 
| [Id](Crm.Sales.SalesOrderPaymentOrdersTemplates.md#id) | guid |  
| [IsAmountWithVAT](Crm.Sales.SalesOrderPaymentOrdersTemplates.md#isamountwithvat) | boolean | True to indicate that the parent document includes VAT and the generated the payment order should be with Is Amount With VAT = true. This setting DOES NOT affect whether the generated amount should include VAT or not, it simply sets the flag in the generated order. [Required] 
| [UpdateForInvoices](Crm.Sales.SalesOrderPaymentOrdersTemplates.md#updateforinvoices) | boolean | Update the payment order when invoices are issued for any of the sales orders lines. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Route](Crm.Sales.SalesOrderPaymentOrdersTemplates.md#route) | [Routes](Systems.Workflow.Routes.md) | The route to which the current option set is assigned. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### CreateForInvoicedAmounts

True to add to the payment order, the part of the amount of the sales order, which is invoiced. [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CreateForNotInvoicedAmounts

True to add to the payment order, the part of the amount of the sales order, which is not included in any invoice. [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsAmountWithVAT

True to indicate that the parent document includes VAT and the generated the payment order should be with Is Amount With VAT = true. This setting DOES NOT affect whether the generated amount should include VAT or not, it simply sets the flag in the generated order. [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UpdateForInvoices

Update the payment order when invoices are issued for any of the sales orders lines. [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Route

The route to which the current option set is assigned. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Routes](Systems.Workflow.Routes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Sales.SalesOrderPaymentOrdersTemplates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Sales.SalesOrderPaymentOrdersTemplates erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_SalesOrderPaymentOrdersTemplates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_SalesOrderPaymentOrdersTemplates?$top=10>

