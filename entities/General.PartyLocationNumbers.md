---
uid: General.PartyLocationNumbers
---
# General.PartyLocationNumbers Entity

**Namespace:** [General](General.md)  

Location numbers for a party. Depending on the partner with which we are doing an exchange, our location number might be different. Entity: Gen_Party_Location_Numbers (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{LocationNumber}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Contacts.Parties](General.Contacts.Parties.md)  
Aggregate Root:  
[General.Contacts.Parties](General.Contacts.Parties.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.PartyLocationNumbers.md#id) | guid |  
| [LocationCodingSystem](General.PartyLocationNumbers.md#locationcodingsystem) | [LocationCodingSystem](General.PartyLocationNumbers.md#locationcodingsystem) | The coding system for which we are defining the location number. `Required` `Default("GLN")` `Filter(multi eq)` 
| [LocationNumber](General.PartyLocationNumbers.md#locationnumber) | string (16) | The location number of Party. `Required` `Filter(multi eq;like)` `ORD` 
| [PartnerLocationNumber](General.PartyLocationNumbers.md#partnerlocationnumber) | string (16) __nullable__ | The location number of the partner party for which we define the main Party location number. The location number of the main Party might be different depending on the location number of the partner party. null means that the location number is not dependent on the partner location number. `Filter(multi eq)` 
| [Significance](General.PartyLocationNumbers.md#significance) | int32 | Order of significance of the location number within the main Party. If there are multiple location numbers, only the most significant is used. 0 is the least significant and higher numbers indicate higher significance. `Required` `Default(0)` `Filter(multi eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PartnerParty](General.PartyLocationNumbers.md#partnerparty) | [Parties](General.Contacts.Parties.md) (nullable) | The party with which we are doing exchange. Depending on the Partner Party, the main Party might have different location number. null means that the location number is not dependent on the Partner Party. `Filter(multi eq)` |
| [Party](General.PartyLocationNumbers.md#party) | [Parties](General.Contacts.Parties.md) | The party for which we are defining the location number. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LocationCodingSystem

The coding system for which we are defining the location number. `Required` `Default("GLN")` `Filter(multi eq)`

_Type_: **[LocationCodingSystem](General.PartyLocationNumbers.md#locationcodingsystem)**  
Allowed values for the `LocationCodingSystem`(General.PartyLocationNumbers.md#locationcodingsystem) data attribute  
_Allowed Values (General.PartyLocationNumbersRepository.LocationCodingSystem Enum Members)_  

| Value | Description |
| ---- | --- |
| GLN | GS1 Global Location Number (GLN). Stored as 'GLN'. <br /> _Database Value:_ 'GLN' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'GLN' |
| Internal | Internal users have access to internal and external content.. Stored as 'INT'. <br /> _Database Value:_ 'INT' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Internal' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **GLN**  

### LocationNumber

The location number of Party. `Required` `Filter(multi eq;like)` `ORD`

_Type_: **string (16)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  
_Maximum Length_: **16**  

### PartnerLocationNumber

The location number of the partner party for which we define the main Party location number. The location number of the main Party might be different depending on the location number of the partner party. null means that the location number is not dependent on the partner location number. `Filter(multi eq)`

_Type_: **string (16) __nullable__**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### Significance

Order of significance of the location number within the main Party. If there are multiple location numbers, only the most significant is used. 0 is the least significant and higher numbers indicate higher significance. `Required` `Default(0)` `Filter(multi eq;ge;le)`

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### PartnerParty

The party with which we are doing exchange. Depending on the Partner Party, the main Party might have different location number. null means that the location number is not dependent on the Partner Party. `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Party

The party for which we are defining the location number. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=General.PartyLocationNumbers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.PartyLocationNumbers erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_PartyLocationNumbers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_PartyLocationNumbers?$top=10>

