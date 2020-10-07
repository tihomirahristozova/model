# Logistics.Procurement.PurchaseOperationTypes

User-defined categorization of the purchase operations. Used to group the purchase control data. Entity: Scm_Purchase_Operation_Types (Introduced in version 18.2.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Procurement.PurchaseOperationTypes.md#Id) | guid |  
| [Code](Logistics.Procurement.PurchaseOperationTypes.md#Code) | string | Unique code of the purchase operation type. [Required] [Filter(multi eq;like)] 
| [Name](Logistics.Procurement.PurchaseOperationTypes.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | Name of the purchase operation type (multilanguage). [Required] [Filter(multi eq;like)] 
| [Notes](Logistics.Procurement.PurchaseOperationTypes.md#Notes) | string (nullable) | Notes for this PurchaseOperationType. [Filter(eq;like)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> Unique code of the purchase operation type. [Required] [Filter(multi eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### Name

> Name of the purchase operation type (multilanguage). [Required] [Filter(multi eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### Notes

> Notes for this PurchaseOperationType. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseOperationTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseOperationTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Procurement.PurchaseOperationTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_PurchaseOperationTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_PurchaseOperationTypes?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Scm_Purchase_Operation_Types?$top=10>

