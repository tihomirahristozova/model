# Crm.Sales.SalesOrder - Entity

Sales order document headers.

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| AdjustmentNumber | int | Consecutive number of the correction that this document is applying to the adjusted document. [Required] (Inherited from General_Document) |
| AdjustmentTime | time | Date/time when the document last has been adjusted by corrective document (Inherited from General_Document) |
| CustomerPurchaseOrderDate | date | 	Issue date of the referent customer purchase order. [Filter(ge;le)] |

## References

| Name | Type | Description |
| ---- | ---- | --- |
| AccessKey |	@Systems.Security.AccessKey | The access key, containing the user permissions for this document. null means that all users have unlimited permissions (Inherited from General_Document) |
| Customer | @Crm.Customer | The primary customer, which placed the sales order. [Required] [Filter(multi eq)] |

## Business Rules

[!list erp.entity=Crm.Sales.SalesOrder erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Sales.SalesOrder erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Sales.SalesOrder erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_SalesOrders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_SalesOrders?$top=10>

Table API:
<https://demodb.my.erp.net/tableapi/Crm_SalesOrders>

## Domain API Operations
(from <https://restdev.erp.bg/ref/#Crm_Sales_SalesOrder> )

| Name | Type | Description |
| ---- | ---- | --- |
| ChangeState |  | Changes the document state to the specified new state
(HTTP Method: POST) |
