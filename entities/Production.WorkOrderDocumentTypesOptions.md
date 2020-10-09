---
uid: Production.WorkOrderDocumentTypesOptions
---
# Production.WorkOrderDocumentTypesOptions

Options for user-defined Work Order document types. Entity: Prd_Work_Order_Document_Types_Options

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.WorkOrderDocumentTypesOptions.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CompletingOutput<br />OrderDocumentType](Production.WorkOrderDocumentTypesOptions.md#completingoutputorderdocumenttype) | [DocumentTypes](General.DocumentTypes.md) (nullable) | User-defined Completing Output Order document type. [Filter(multi eq)] |
| [DocumentType](Production.WorkOrderDocumentTypesOptions.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | User-defined Work Order document type. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### CompletingOutputOrderDocumentType

> User-defined Completing Output Order document type. [Filter(multi eq)]

_Type_: **[DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

> User-defined Work Order document type. [Required] [Filter(multi eq)]

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Production.WorkOrderDocumentTypesOptions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.WorkOrderDocumentTypesOptions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.WorkOrderDocumentTypesOptions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_WorkOrderDocumentTypesOptions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_WorkOrderDocumentTypesOptions?$top=10>

