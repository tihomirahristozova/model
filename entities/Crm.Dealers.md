---
uid: Crm.Dealers
---
# Crm.Dealers Entity

**Namespace:** [Crm](Crm.md)  

External dealers. Entity: Crm_Dealers

## Default Visualization
Default Display Text Format:  
_{Id}: {PartyId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.Dealers](Crm.Dealers.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FromDate](Crm.Dealers.md#fromdate) | datetime __nullable__ | Start of the dealer relationship. `Default(Today)` `Filter(ge;le)` 
| [Id](Crm.Dealers.md#id) | guid |  
| [Notes](Crm.Dealers.md#notes) | string (254) __nullable__ | Notes for this Dealer. 
| [ThruDate](Crm.Dealers.md#thrudate) | datetime __nullable__ | Termination date of the dealership. null for active dealers. `Filter(ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Crm.Dealers.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The enterprise company for which this dealer is recorded. `Filter(multi eq)` |
| [Party](Crm.Dealers.md#party) | [Parties](General.Contacts.Parties.md) | The base party record of the dealer. `Required` `Filter(multi eq)` |


## Attribute Details

### FromDate

Start of the dealer relationship. `Default(Today)` `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this Dealer.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ThruDate

Termination date of the dealership. null for active dealers. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

The enterprise company for which this dealer is recorded. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Party

The base party record of the dealer. `Required` `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Dealers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Dealers erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Dealers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Dealers?$top=10>

