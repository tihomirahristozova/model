---
uid: General.Geography.AdministrativeRegions
---
# General.Geography.AdministrativeRegions Entity

**Namespace:** [General.Geography](General.Geography.md)  

Hierarchical structure of the legally defined administrative regions. Administrative regions are sub-divisions of the countries. Entity: Gen_Administrative_Regions

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Code; Name_  
Code Data Member:  
_Code_  
Name Data Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Geography.AdministrativeRegions](General.Geography.AdministrativeRegions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.Geography.AdministrativeRegions.md#code) | string (16) | Administrative code of country territorial subdivision. `Required` `Filter(eq;like)` 
| [DisplayText](General.Geography.AdministrativeRegions.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [FullPath](General.Geography.AdministrativeRegions.md#fullpath) | string (254) __nullable__ | Full identification path of the current country territorial subdivision. `Filter(eq;like)` 
| [Id](General.Geography.AdministrativeRegions.md#id) | guid |  
| [Name](General.Geography.AdministrativeRegions.md#name) | [MultilanguageString (254)](../data-types.md#multilanguagestring) | Name of country territorial subdivision. `Required` `Filter(like)` 
| [ObjectVersion](General.Geography.AdministrativeRegions.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [ParentFullPath](General.Geography.AdministrativeRegions.md#parentfullpath) | string (254) __nullable__ | Parent region of the current territorial subdivision. `Filter(eq;like)` 
| [ValidFrom](General.Geography.AdministrativeRegions.md#validfrom) | date __nullable__ | Start date of validity of this administrative division. null when the starting date is unknown in the past. `Filter(ge;le)` 
| [ValidTo](General.Geography.AdministrativeRegions.md#validto) | date __nullable__ | End date of validity of this administative division. null when the division is still active or ending date is unknown. `Filter(ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Country](General.Geography.AdministrativeRegions.md#country) | [Countries](General.Geography.Countries.md) | Country of the territorial subdivision. `Required` `Filter(multi eq)` |


## Attribute Details

### Code

Administrative code of country territorial subdivision. `Required` `Filter(eq;like)`

_Type_: **string (16)**  
_Category_: **System**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### FullPath

Full identification path of the current country territorial subdivision. `Filter(eq;like)`

_Type_: **string (254) __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of country territorial subdivision. `Required` `Filter(like)`

_Type_: **[MultilanguageString (254)](../data-types.md#multilanguagestring)**  
_Category_: **System**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ParentFullPath

Parent region of the current territorial subdivision. `Filter(eq;like)`

_Type_: **string (254) __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ValidFrom

Start date of validity of this administrative division. null when the starting date is unknown in the past. `Filter(ge;le)`

_Type_: **date __nullable__**  
_Category_: **System**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ValidTo

End date of validity of this administative division. null when the division is still active or ending date is unknown. `Filter(ge;le)`

_Type_: **date __nullable__**  
_Category_: **System**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### Country

Country of the territorial subdivision. `Required` `Filter(multi eq)`

_Type_: **[Countries](General.Geography.Countries.md)**  
_Indexed_: **True**  
_Category_: **System**  
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


### CreateNotification

Creates a notification a sends a real time event to the user.  
_Return Type_: **void**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  

**Parameters**  
  * **user**  
    The user.  
    _Type_: [Users](Systems.Security.Users.md)  

  * **notificationClass**  
    The notification class.  
    _Type_: string  

  * **subject**  
    The subject.  
    _Type_: string  


### CreateCopy

Duplicates the object and its child objects belonging to the same aggregate.              The duplicated objects are not saved to the data source but remain in the same transaction as the original object.  
_Return Type_: **EntityObject**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  


## Business Rules

[!list limit=1000 erp.entity=General.Geography.AdministrativeRegions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Geography.AdministrativeRegions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Geography_AdministrativeRegions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Geography_AdministrativeRegions?$top=10>

