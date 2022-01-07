---
uid: Crm.Marketing.Competitors
---
# Crm.Marketing.Competitors Entity

**Namespace:** [Crm.Marketing](Crm.Marketing.md)  

Competitors to our marketing solutions. Entity: Crm_Competitors (Introduced in version 22.1.4.70)

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Name_  
Name Data Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.Marketing.Competitors](Crm.Marketing.Competitors.md)  
  * [Crm.Marketing.CompetitorSolutions](Crm.Marketing.CompetitorSolutions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](Crm.Marketing.Competitors.md#displaytext) | string |  
| [Id](Crm.Marketing.Competitors.md#id) | guid |  
| [Name](Crm.Marketing.Competitors.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this Competitor. `Required` `Filter(like)` 
| [Notes](Crm.Marketing.Competitors.md#notes) | string (max) __nullable__ | Notes for this Competitor. 
| [ObjectVersion](Crm.Marketing.Competitors.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Crm.Marketing.Competitors.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | Our enterprise company, for which we are defining the competitor. null means that the competitor is defined for all the companies in the ERP instance. `Filter(multi eq)` |
| [Party](Crm.Marketing.Competitors.md#party) | [Parties](General.Contacts.Parties.md) (nullable) | When not null, specifies the party of the competitor. `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Solutions | [CompetitorSolutions](Crm.Marketing.CompetitorSolutions.md) | List of `CompetitorSolution`(Crm.Marketing.CompetitorSolutions.md) child objects, based on the `Crm.Marketing.CompetitorSolution.Competitor`(Crm.Marketing.CompetitorSolutions.md#competitor) back reference 


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

### Name

The name of this Competitor. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

Notes for this Competitor.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### EnterpriseCompany

Our enterprise company, for which we are defining the competitor. null means that the competitor is defined for all the companies in the ERP instance. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Party

When not null, specifies the party of the competitor. `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
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

[!list limit=1000 erp.entity=Crm.Marketing.Competitors erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.Competitors erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_Competitors?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_Competitors?$top=10>

