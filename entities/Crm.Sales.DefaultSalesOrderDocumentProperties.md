---
uid: Crm.Sales.DefaultSalesOrderDocumentProperties
---
# Crm.Sales.DefaultSalesOrderDocumentProperties

User-defined properties which shall be copied from the customer to the document for new documents of the specified document type. Entity: Crm_Default_Sales_Order_Document_Properties

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Sales.DefaultSalesOrderDocumentProperties.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CustomerProperty](Crm.Sales.DefaultSalesOrderDocumentProperties.md#customerproperty) | [General.CustomProperties](General.CustomProperties.md) | The user-defined customer property that shall be copied. [Required] [Filter(multi eq)] |
| [DocumentProperty](Crm.Sales.DefaultSalesOrderDocumentProperties.md#documentproperty) | [General.CustomProperties](General.CustomProperties.md) | The user-defined document property in which to copy the customers property value. [Required] [Filter(multi eq)] |
| [DocumentType](Crm.Sales.DefaultSalesOrderDocumentProperties.md#documenttype) | [General.DocumentTypes](General.DocumentTypes.md) | The document type for which the current definitions apply. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### CustomerProperty

> The user-defined customer property that shall be copied. [Required] [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentProperty

> The user-defined document property in which to copy the customers property value. [Required] [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

> The document type for which the current definitions apply. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Sales.DefaultSalesOrderDocumentProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Sales.DefaultSalesOrderDocumentProperties erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Sales.DefaultSalesOrderDocumentProperties erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_DefaultSalesOrderDocumentProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_DefaultSalesOrderDocumentProperties?$top=10>

