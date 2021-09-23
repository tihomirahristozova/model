---
uid: General.DocumentFulfillments
---
# General.DocumentFulfillments Entity

**Namespace:** [General](General.md)  

Fulfillment ledger for documents. Entity: Gen_Document_Fulfillments (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{DestinationEntityName:T}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.DocumentFulfillments](General.DocumentFulfillments.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationTimeUtc](General.DocumentFulfillments.md#creationtimeutc) | datetime | The exact time in UTC, when the fulfillment was created in the system. `Required` `Default(NowUtc)` `Filter(multi eq;ge;le)` 
| [DestinationEntityName](General.DocumentFulfillments.md#destinationentityname) | string (64) | The name of the entity which fulfills the line. Used to differentiate between different fulfillment types. For example, sales order line can be fulfilled, for different purposes, by store order line and invoice order line. `Required` `Default("")` `Filter(eq)` `Introduced in version 22.1.4.7` 
| [DocumentLineId](General.DocumentFulfillments.md#documentlineid) | guid | The Id of the fulfilled line within the document. The attribute contains the Id and is not a reference, because it references different entities depending on document entity type and line type. `Required` `Filter(multi eq)` 
| [FulfillmentType](General.DocumentFulfillments.md#fulfillmenttype) | [FulfillmentType](General.DocumentFulfillments.md#fulfillmenttype) | Type of fulfillment: P=Planned; C=Completed. `Required` `Filter(multi eq)` `Introduced in version 21.1.1.26` 
| [Id](General.DocumentFulfillments.md#id) | guid |  
| [IsFinal](General.DocumentFulfillments.md#isfinal) | boolean | Specifies whether this fulfillment finalizes the line, regardless of any remaining quantities. `Required` `Filter(eq)` 
| [LineNo](General.DocumentFulfillments.md#lineno) | int32 __nullable__ | Line number. Used for human-readability of the fulfillment. null if the lines do not support line numbers or the line number is unknown. `Filter(multi eq;ge;le)` `Introduced in version 21.1.1.26` 
| [LineType](General.DocumentFulfillments.md#linetype) | string (1) | Detail (line) type, for example materials, services, etc. L=Line. Other values are defined by the document entity type. `Required` `Default("L")` `Filter(multi eq)` `Introduced in version 21.1.1.26` 
| [QuantityBase](General.DocumentFulfillments.md#quantitybase) | decimal (12, 3) | Fulfilled quantity in the base measurement unit of the product. `Required` `Filter(multi eq;ge;le)` `Introduced in version 21.1.1.33` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationUser](General.DocumentFulfillments.md#creationuser) | [Users](Systems.Security.Users.md) | The user, who created the record. `Required` `Filter(multi eq)` |
| [Document](General.DocumentFulfillments.md#document) | [Documents](General.Documents.md) | The Document, which is fulfilled. `Required` `Filter(multi eq)` `Introduced in version 21.1.1.26` |


## Attribute Details

### CreationTimeUtc

The exact time in UTC, when the fulfillment was created in the system. `Required` `Default(NowUtc)` `Filter(multi eq;ge;le)`

_Type_: **datetime**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTimeUtc**  

### DestinationEntityName

The name of the entity which fulfills the line. Used to differentiate between different fulfillment types. For example, sales order line can be fulfilled, for different purposes, by store order line and invoice order line. `Required` `Default("")` `Filter(eq)` `Introduced in version 22.1.4.7`

_Type_: **string (64)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  
_Default Value_: ****  

### DocumentLineId

The Id of the fulfilled line within the document. The attribute contains the Id and is not a reference, because it references different entities depending on document entity type and line type. `Required` `Filter(multi eq)`

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### FulfillmentType

Type of fulfillment: P=Planned; C=Completed. `Required` `Filter(multi eq)` `Introduced in version 21.1.1.26`

_Type_: **[FulfillmentType](General.DocumentFulfillments.md#fulfillmenttype)**  
Allowed values for the `FulfillmentType`(General.DocumentFulfillments.md#fulfillmenttype) data attribute  
_Allowed Values (General.DocumentFulfillmentsRepository.FulfillmentType Enum Members)_  

| Value | Description |
| ---- | --- |
| Planned | Planned value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Planned' |
| Completed | Completed value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Completed' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsFinal

Specifies whether this fulfillment finalizes the line, regardless of any remaining quantities. `Required` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### LineNo

Line number. Used for human-readability of the fulfillment. null if the lines do not support line numbers or the line number is unknown. `Filter(multi eq;ge;le)` `Introduced in version 21.1.1.26`

_Type_: **int32 __nullable__**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

### LineType

Detail (line) type, for example materials, services, etc. L=Line. Other values are defined by the document entity type. `Required` `Default("L")` `Filter(multi eq)` `Introduced in version 21.1.1.26`

_Type_: **string (1)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **1**  
_Default Value_: **L**  

### QuantityBase

Fulfilled quantity in the base measurement unit of the product. `Required` `Filter(multi eq;ge;le)` `Introduced in version 21.1.1.33`

_Type_: **decimal (12, 3)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### CreationUser

The user, who created the record. `Required` `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Document

The Document, which is fulfilled. `Required` `Filter(multi eq)` `Introduced in version 21.1.1.26`

_Type_: **[Documents](General.Documents.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentFulfillments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentFulfillments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentFulfillments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentFulfillments?$top=10>

