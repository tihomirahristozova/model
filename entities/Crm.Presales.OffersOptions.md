---
uid: Crm.Presales.OffersOptions
---
# Crm.Presales.OffersOptions Entity

**Namespace:** [Crm.Presales](Crm.Presales.md)  

Contains options for user defined document types for Offers. Entity: Crm_Offers_Options

## Default Visualization
Default Display Text Format:  
_{DocumentType.TypeName} : {DocumentType.Code}_  
Default Search Member:  
_DocumentType.TypeName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.DocumentTypes](General.DocumentTypes.md)  
Aggregate Root:  
[General.DocumentTypes](General.DocumentTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Presales.OffersOptions.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DealDocumentType](Crm.Presales.OffersOptions.md#dealdocumenttype) | [DocumentTypes](General.DocumentTypes.md) (nullable) | If filled then new opportunities (deals) from the specified type will be created automatically for the offers that aren't assigned to existing opportunities. Used for automating opportunity management. `Filter(multi eq)` |
| [DocumentType](Crm.Presales.OffersOptions.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type for which the offer option applies. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### DealDocumentType

If filled then new opportunities (deals) from the specified type will be created automatically for the offers that aren't assigned to existing opportunities. Used for automating opportunity management. `Filter(multi eq)`

_Type_: **[DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

The document type for which the offer option applies. `Required` `Filter(multi eq)` `Owner`

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Presales.OffersOptions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Presales.OffersOptions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Presales_OffersOptions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Presales_OffersOptions?$top=10>

