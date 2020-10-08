---
uid: Finance.Vat.DealTypes
---
# Finance.Vat.DealTypes

Contains deal types supported by the system as well as user-defined types. Entity: VAT_Deal_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Vat.DealTypes.md#Id) | guid |  
| [Name](Finance.Vat.DealTypes.md#Name) | string | Description of the deal type. [Required] [Filter(eq;like)] 
| [EntryType](Finance.Vat.DealTypes.md#EntryType) | [Finance.Vat.DealTypesRepository.EntryType](Finance.Vat.DealTypes.md#EntryType) | Type of the VAT entries, which are made for this deal type. S=Sales, P=Purchases. [Required] [Filter(eq)] 
| [IsSystem](Finance.Vat.DealTypes.md#IsSystem) | boolean | Is_System is True for those deal types that are managed by the system via update procedures and cannot be edited by the user. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Country](Finance.Vat.DealTypes.md#Country) | [General.Geography.Countries](General.Geography.Countries.md) | The country for which this deal type applies. The country is matched against the country of the enterprise company. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Name

> Description of the deal type. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### EntryType

> Type of the VAT entries, which are made for this deal type. S=Sales, P=Purchases. [Required] [Filter(eq)]

_Type_: **[Finance.Vat.DealTypesRepository.EntryType](Finance.Vat.DealTypes.md#EntryType)**  
Allowed values for the [EntryType](Finance.Vat.DealTypes.md#EntryType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Purchases | Purchases value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Purchases' |
| Sales | Sales value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Sales' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### IsSystem

> Is_System is True for those deal types that are managed by the system via update procedures and cannot be edited by the user. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### Country

> The country for which this deal type applies. The country is matched against the country of the enterprise company. [Required] [Filter(multi eq)]

_Type_: **[General.Geography.Countries](General.Geography.Countries.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Vat.DealTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Vat.DealTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Vat.DealTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Vat_DealTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Vat_DealTypes?$top=10>

