---
uid: Crm.Sales.DefaultSalesOrderDocumentProperties
---
# Crm.Sales.DefaultSalesOrderDocumentProperties Entity

**Namespace:** [Crm.Sales](Crm.Sales.md)  

User-defined properties which shall be copied from the customer to the document for new documents of the specified document type. Entity: Crm_Default_Sales_Order_Document_Properties

## Default Visualization
Default Display Text Format:  
_{DocumentType.EntityName:T} : {DocumentType.Code}_  
Default Search Member:  
_DocumentType.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.DocumentTypes](General.DocumentTypes.md)  
Aggregate Root:  
[General.DocumentTypes](General.DocumentTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Sales.DefaultSalesOrderDocumentProperties.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CustomerProperty](Crm.Sales.DefaultSalesOrderDocumentProperties.md#customerproperty) | [CustomProperties](General.CustomProperties.md) | The user-defined customer property that shall be copied. `Required` `Filter(multi eq)` |
| [DocumentProperty](Crm.Sales.DefaultSalesOrderDocumentProperties.md#documentproperty) | [CustomProperties](General.CustomProperties.md) | The user-defined document property in which to copy the customers property value. `Required` `Filter(multi eq)` |
| [DocumentType](Crm.Sales.DefaultSalesOrderDocumentProperties.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type for which the current definitions apply. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### CustomerProperty

The user-defined customer property that shall be copied. `Required` `Filter(multi eq)`

_Type_: **[CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentProperty

The user-defined document property in which to copy the customers property value. `Required` `Filter(multi eq)`

_Type_: **[CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

The document type for which the current definitions apply. `Required` `Filter(multi eq)` `Owner`

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Sales.DefaultSalesOrderDocumentProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Sales.DefaultSalesOrderDocumentProperties erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_DefaultSalesOrderDocumentProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_DefaultSalesOrderDocumentProperties?$top=10>

