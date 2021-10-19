---
uid: General.DocumentTypeEnterpriseCompanies
---
# General.DocumentTypeEnterpriseCompanies Entity

**Namespace:** [General](General.md)  

Specifies the visibility (availability) of the document type for the different enterprise companies. Entity: Gen_Document_Type_Enterprise_Companies

## Default Visualization
Default Display Text Format:  
_{DocumentType.EntityName}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.DocumentTypes](General.DocumentTypes.md)  
Aggregate Root:  
[General.DocumentTypes](General.DocumentTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentTypeEnterpriseCompanies.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](General.DocumentTypeEnterpriseCompanies.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type for which visibility (availability) is set. `Required` `Filter(multi eq)` `Owner` |
| [EnterpriseCompany](General.DocumentTypeEnterpriseCompanies.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company for which the current document type is visible (available). `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### DocumentType

The document type for which visibility (availability) is set. `Required` `Filter(multi eq)` `Owner`

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### EnterpriseCompany

The enterprise company for which the current document type is visible (available). `Required` `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentTypeEnterpriseCompanies erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentTypeEnterpriseCompanies erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentTypeEnterpriseCompanies?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentTypeEnterpriseCompanies?$top=10>

