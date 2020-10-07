# Crm.Dealers

External dealers. Entity: Crm_Dealers

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Dealers.md#Id) | guid |  
| [FromDate](Crm.Dealers.md#FromDate) | datetime (nullable) | Start of the dealer relationship. [Default(Today)] [Filter(ge;le)] 
| [Notes](Crm.Dealers.md#Notes) | string (nullable) | Notes for this Dealer. 
| [ThruDate](Crm.Dealers.md#ThruDate) | datetime (nullable) | Termination date of the dealership. null for active dealers. [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Crm.Dealers.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The enterprise company for which this dealer is recorded. [Filter(multi eq)] |
| [Party](Crm.Dealers.md#Party) | [General.Contacts.Parties](General.Contacts.Parties.md) | The base party record of the dealer. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FromDate

> Start of the dealer relationship. [Default(Today)] [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### Notes

> Notes for this Dealer.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ThruDate

> Termination date of the dealership. null for active dealers. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company for which this dealer is recorded. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Party

> The base party record of the dealer. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Dealers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Dealers erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Dealers erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Dealers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Dealers?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Dealers?$top=10>

