---
uid: Logistics.Inventory.TransactionEntryTemplates
---
# Logistics.Inventory.TransactionEntryTemplates

Obsolete. Not used. Entity: Inv_Transaction_Entry_Templates

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.TransactionEntryTemplates.md#Id) | guid |  
| [DocumentNotesFixedText](Logistics.Inventory.TransactionEntryTemplates.md#DocumentNotesFixedText) | string (nullable) | Specifies the text for the document notes in the created entry in the VAT ledgers, in case the source is set to be fixed text. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DealType](Logistics.Inventory.TransactionEntryTemplates.md#DealType) | [Finance.Vat.DealTypes](Finance.Vat.DealTypes.md) | Obsolete. Not used. [Required] [Filter(multi eq)] |
| [Route](Logistics.Inventory.TransactionEntryTemplates.md#Route) | [Systems.Workflow.Routes](Systems.Workflow.Routes.md) | Obsolete. Not used. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DocumentNotesFixedText

> Specifies the text for the document notes in the created entry in the VAT ledgers, in case the source is set to be fixed text.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### DealType

> Obsolete. Not used. [Required] [Filter(multi eq)]

_Type_: **[Finance.Vat.DealTypes](Finance.Vat.DealTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Route

> Obsolete. Not used. [Required] [Filter(multi eq)]

_Type_: **[Systems.Workflow.Routes](Systems.Workflow.Routes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.TransactionEntryTemplates erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.TransactionEntryTemplates erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.TransactionEntryTemplates erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_TransactionEntryTemplates?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_TransactionEntryTemplates?$top=10>

