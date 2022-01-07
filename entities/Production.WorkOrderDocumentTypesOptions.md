---
uid: Production.WorkOrderDocumentTypesOptions
---
# Production.WorkOrderDocumentTypesOptions Entity

**Namespace:** [Production](Production.md)  

Options for user-defined Work Order document types. Entity: Prd_Work_Order_Document_Types_Options

## Default Visualization
Default Display Text Format:  
_{Id}: {DocumentTypeId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Production.WorkOrderDocumentTypesOptions](Production.WorkOrderDocumentTypesOptions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](Production.WorkOrderDocumentTypesOptions.md#displaytext) | string |  
| [Id](Production.WorkOrderDocumentTypesOptions.md#id) | guid |  
| [ObjectVersion](Production.WorkOrderDocumentTypesOptions.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CompletingOutput<br />OrderDocumentType](Production.WorkOrderDocumentTypesOptions.md#completingoutputorderdocumenttype) | [DocumentTypes](General.DocumentTypes.md) (nullable) | User-defined Completing Output Order document type. `Filter(multi eq)` |
| [DocumentType](Production.WorkOrderDocumentTypesOptions.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | User-defined Work Order document type. `Required` `Filter(multi eq)` |


## Attribute Details

### DisplayText

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### CompletingOutputOrderDocumentType

User-defined Completing Output Order document type. `Filter(multi eq)`

_Type_: **[DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

User-defined Work Order document type. `Required` `Filter(multi eq)`

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Production.WorkOrderDocumentTypesOptions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Production.WorkOrderDocumentTypesOptions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_WorkOrderDocumentTypesOptions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_WorkOrderDocumentTypesOptions?$top=10>

