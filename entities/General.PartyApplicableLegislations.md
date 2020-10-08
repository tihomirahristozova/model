---
uid: General.PartyApplicableLegislations
---
# General.PartyApplicableLegislations

Specifies a legislation, which is applicable for a party. A single party can have more than one applicable legislations. Entity: Gen_Party_Applicable_Legislations (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.PartyApplicableLegislations.md#Id) | guid |  
| [ApplicableLegislation](General.PartyApplicableLegislations.md#ApplicableLegislation) | [General.PartyApplicableLegislationsRepository.ApplicableLegislation](General.PartyApplicableLegislations.md#ApplicableLegislation) | A legislation, which applies to the specified party. The list of legislations is system defined, and contains legislations for which system rules are currently defined. For example: US, UK, EU, DE, FR, ES, IT, BG, MK, RO, GR, etc. [Required] [Filter(multi eq)] [ORD] 
| [Notes](General.PartyApplicableLegislations.md#Notes) | string (nullable) | Notes for this PartyApplicableLegislation. [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Party](General.PartyApplicableLegislations.md#Party) | [General.Contacts.Parties](General.Contacts.Parties.md) | The [Party](General.Contacts.Parties.md) to which this PartyApplicableLegislation belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ApplicableLegislation

> A legislation, which applies to the specified party. The list of legislations is system defined, and contains legislations for which system rules are currently defined. For example: US, UK, EU, DE, FR, ES, IT, BG, MK, RO, GR, etc. [Required] [Filter(multi eq)] [ORD]

_Type_: **[General.PartyApplicableLegislationsRepository.ApplicableLegislation](General.PartyApplicableLegislations.md#ApplicableLegislation)**  
Allowed values for the [ApplicableLegislation](General.PartyApplicableLegislations.md#ApplicableLegislation) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| UnitedArabEmirates | UnitedArabEmirates value. Stored as 'AE'. <br /> _Database Value:_ 'AE' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'UnitedArabEmirates' |
| Australia | Australia value. Stored as 'AU'. <br /> _Database Value:_ 'AU' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Australia' |
| Bulgaria | Bulgaria value. Stored as 'BG'. <br /> _Database Value:_ 'BG' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Bulgaria' |
| Canada | Canada value. Stored as 'CA'. <br /> _Database Value:_ 'CA' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Canada' |
| China | China value. Stored as 'CN'. <br /> _Database Value:_ 'CN' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'China' |
| CzechRepublic | CzechRepublic value. Stored as 'CZ'. <br /> _Database Value:_ 'CZ' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'CzechRepublic' |
| Germany | Germany value. Stored as 'DE'. <br /> _Database Value:_ 'DE' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'Germany' |
| Spain | Spain value. Stored as 'ES'. <br /> _Database Value:_ 'ES' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'Spain' |
| EuropeanUnion | EuropeanUnion value. Stored as 'EU'. <br /> _Database Value:_ 'EU' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'EuropeanUnion' |
| France | France value. Stored as 'FR'. <br /> _Database Value:_ 'FR' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'France' |
| Greece | Greece value. Stored as 'GR'. <br /> _Database Value:_ 'GR' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Greece' |
| Hungary | Hungary value. Stored as 'HU'. <br /> _Database Value:_ 'HU' <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'Hungary' |
| India | India value. Stored as 'IN'. <br /> _Database Value:_ 'IN' <br /> _Model Value:_ 12 <br /> _Domain API Value:_ 'India' |
| Italy | Italy value. Stored as 'IT'. <br /> _Database Value:_ 'IT' <br /> _Model Value:_ 13 <br /> _Domain API Value:_ 'Italy' |
| Japan | Japan value. Stored as 'JP'. <br /> _Database Value:_ 'JP' <br /> _Model Value:_ 14 <br /> _Domain API Value:_ 'Japan' |
| Macedonia | Macedonia value. Stored as 'MK'. <br /> _Database Value:_ 'MK' <br /> _Model Value:_ 15 <br /> _Domain API Value:_ 'Macedonia' |
| Poland | Poland value. Stored as 'PL'. <br /> _Database Value:_ 'PL' <br /> _Model Value:_ 16 <br /> _Domain API Value:_ 'Poland' |
| Portugal | Portugal value. Stored as 'PT'. <br /> _Database Value:_ 'PT' <br /> _Model Value:_ 17 <br /> _Domain API Value:_ 'Portugal' |
| Romania | Romania value. Stored as 'RO'. <br /> _Database Value:_ 'RO' <br /> _Model Value:_ 18 <br /> _Domain API Value:_ 'Romania' |
| Serbia | Serbia value. Stored as 'RS'. <br /> _Database Value:_ 'RS' <br /> _Model Value:_ 19 <br /> _Domain API Value:_ 'Serbia' |
| Russia | Russia value. Stored as 'RU'. <br /> _Database Value:_ 'RU' <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'Russia' |
| Turkey | Turkey value. Stored as 'TR'. <br /> _Database Value:_ 'TR' <br /> _Model Value:_ 21 <br /> _Domain API Value:_ 'Turkey' |
| UnitedKingdom | UnitedKingdom value. Stored as 'UK'. <br /> _Database Value:_ 'UK' <br /> _Model Value:_ 22 <br /> _Domain API Value:_ 'UnitedKingdom' |
| UnitedStates | UnitedStates value. Stored as 'US'. <br /> _Database Value:_ 'US' <br /> _Model Value:_ 23 <br /> _Domain API Value:_ 'UnitedStates' |
| SouthAfrica | SouthAfrica value. Stored as 'ZA'. <br /> _Database Value:_ 'ZA' <br /> _Model Value:_ 24 <br /> _Domain API Value:_ 'SouthAfrica' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **True**  

### Notes

> Notes for this PartyApplicableLegislation. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### Party

> The [Party](General.Contacts.Parties.md) to which this PartyApplicableLegislation belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.PartyApplicableLegislations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.PartyApplicableLegislations erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.PartyApplicableLegislations erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_PartyApplicableLegislations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_PartyApplicableLegislations?$top=10>

