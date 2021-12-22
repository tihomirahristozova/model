---
uid: Finance.Vat.DealTypes
---
# Finance.Vat.DealTypes Entity

**Namespace:** [Finance.Vat](Finance.Vat.md)  

Contains deal types supported by the system as well as user-defined types. Entity: VAT_Deal_Types

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Vat.DealTypes](Finance.Vat.DealTypes.md)  
  * [Finance.Vat.DealTypeDocumentAmounts](Finance.Vat.DealTypeDocumentAmounts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EntryType](Finance.Vat.DealTypes.md#entrytype) | [EntryType](Finance.Vat.DealTypes.md#entrytype) | Type of the VAT entries, which are made for this deal type. S=Sales, P=Purchases. `Required` `Filter(eq)` 
| [Id](Finance.Vat.DealTypes.md#id) | guid |  
| [IsSystem](Finance.Vat.DealTypes.md#issystem) | boolean | Is_System is True for those deal types that are managed by the system via update procedures and cannot be edited by the user. `Required` `Default(false)` `Filter(eq)` `ReadOnly` 
| [Name](Finance.Vat.DealTypes.md#name) | string (254) | Description of the deal type. `Required` `Filter(eq;like)` 
| [ObjectVersion](Finance.Vat.DealTypes.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Country](Finance.Vat.DealTypes.md#country) | [Countries](General.Geography.Countries.md) | The country for which this deal type applies. The country is matched against the country of the enterprise company. `Required` `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| DocumentAmounts | [DealTypeDocumentAmounts](Finance.Vat.DealTypeDocumentAmounts.md) | List of `DealTypeDocumentAmount`(Finance.Vat.DealTypeDocumentAmounts.md) child objects, based on the `Finance.Vat.DealTypeDocumentAmount.DealType`(Finance.Vat.DealTypeDocumentAmounts.md#dealtype) back reference 


## Attribute Details

### EntryType

Type of the VAT entries, which are made for this deal type. S=Sales, P=Purchases. `Required` `Filter(eq)`

_Type_: **[EntryType](Finance.Vat.DealTypes.md#entrytype)**  
Allowed values for the `EntryType`(Finance.Vat.DealTypes.md#entrytype) data attribute  
_Allowed Values (Finance.Vat.DealTypesRepository.EntryType Enum Members)_  

| Value | Description |
| ---- | --- |
| Purchases | Purchases value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Purchases' |
| Sales | Sales value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Sales' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsSystem

Is_System is True for those deal types that are managed by the system via update procedures and cannot be edited by the user. `Required` `Default(false)` `Filter(eq)` `ReadOnly`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

Description of the deal type. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### Country

The country for which this deal type applies. The country is matched against the country of the enterprise company. `Required` `Filter(multi eq)`

_Type_: **[Countries](General.Geography.Countries.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Vat.DealTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Vat.DealTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Vat_DealTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Vat_DealTypes?$top=10>

