---
uid: Projects.ProjectRiskDiscussion
---
# Projects.ProjectRiskDiscussion Entity

**Namespace:** [Projects](Projects.md)  

Contains discussions on project risks. Entity: Prj_Project_Risk_Discussion

## Default Visualization
Default Display Text Format:  
_{ProjectRisk.RiskName}_  
Default Search Members:  
_ProjectRisk.RiskName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Projects.ProjectRisks](Projects.ProjectRisks.md)  
Aggregate Root:  
[Projects.Projects](Projects.Projects.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ContributionTime](Projects.ProjectRiskDiscussion.md#contributiontime) | datetime | The time, when the message was contributed. `Required` `Default(Now)` `Filter(eq)` `ReadOnly` 
| [Id](Projects.ProjectRiskDiscussion.md#id) | guid |  
| [LastEditTime](Projects.ProjectRiskDiscussion.md#lastedittime) | datetime __nullable__ | Contains the last edit time of the message. null if the message was never edited. `Filter(eq)` `ReadOnly` 
| [Message](Projects.ProjectRiskDiscussion.md#message) | string (max) | The contents of the message. `Required` 
| [ObjectVersion](Projects.ProjectRiskDiscussion.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ContributedByUser](Projects.ProjectRiskDiscussion.md#contributedbyuser) | [Users](Systems.Security.Users.md) | The user, who contributed (wrote) the message. `Required` `Filter(multi eq)` `ReadOnly` |
| [ProjectRisk](Projects.ProjectRiskDiscussion.md#projectrisk) | [ProjectRisks](Projects.ProjectRisks.md) | The <see cref="ProjectRisk"/> to which this ProjectRiskDiscussion belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### ContributionTime

The time, when the message was contributed. `Required` `Default(Now)` `Filter(eq)` `ReadOnly`

_Type_: **datetime**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LastEditTime

Contains the last edit time of the message. null if the message was never edited. `Filter(eq)` `ReadOnly`

_Type_: **datetime __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Message

The contents of the message. `Required`

_Type_: **string (max)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### ContributedByUser

The user, who contributed (wrote) the message. `Required` `Filter(multi eq)` `ReadOnly`

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProjectRisk

The <see cref="ProjectRisk"/> to which this ProjectRiskDiscussion belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ProjectRisks](Projects.ProjectRisks.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  


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

[!list limit=1000 erp.entity=Projects.ProjectRiskDiscussion erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Projects.ProjectRiskDiscussion erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectRiskDiscussion?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectRiskDiscussion?$top=10>

