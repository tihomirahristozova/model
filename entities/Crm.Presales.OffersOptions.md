---
uid: Crm.Presales.OffersOptions
---
# Crm.Presales.OffersOptions Entity

Contains options for user defined document types for Offers. Entity: Crm_Offers_Options

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Presales.OffersOptions.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DealDocumentType](Crm.Presales.OffersOptions.md#dealdocumenttype) | [DocumentTypes](General.DocumentTypes.md) (nullable) | If filled then new opportunities (deals) from the specified type will be created automatically for the offers that aren't assigned to existing opportunities. Used for automating opportunity management. [Filter(multi eq)] |
| [DocumentType](Crm.Presales.OffersOptions.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type for which the offer option applies. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### DealDocumentType

If filled then new opportunities (deals) from the specified type will be created automatically for the offers that aren't assigned to existing opportunities. Used for automating opportunity management. [Filter(multi eq)]

_Type_: **[DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

The document type for which the offer option applies. [Required] [Filter(multi eq)] [Owner]

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Presales.OffersOptions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Presales.OffersOptions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Presales_OffersOptions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Presales_OffersOptions?$top=10>

