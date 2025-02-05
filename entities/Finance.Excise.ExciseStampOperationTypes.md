---
uid: Finance.Excise.ExciseStampOperationTypes
---
# Finance.Excise.ExciseStampOperationTypes Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

Specifies the type of the Excise Stamp operation. Entity: Exc_Excise_Stamp_Operation_Types (Introduced in version 22.1.5.85)

## Default Visualization
Default Display Text Format:  
_{Code}: {Name}_  
Default Search Members:  
_Code; Name_  
Code Data Member:  
_Code_  
Name Data Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Excise.ExciseStampOperationTypes](Finance.Excise.ExciseStampOperationTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Box1Effect](Finance.Excise.ExciseStampOperationTypes.md#box1effect) | [ExciseStampOperation<br />TypeEnum](Finance.Excise.ExciseStampOperationTypes.md#box1effect) | Specifies how the operation changes the Excise Stamp availability in the correspondent Box. The boxes are used to report the availability of excise stamps in the relevant locations according to the requirements of the customs administration. `Required` `Default("N")` 
| [Box2Effect](Finance.Excise.ExciseStampOperationTypes.md#box2effect) | [ExciseStampOperation<br />TypeEnum](Finance.Excise.ExciseStampOperationTypes.md#box2effect) | Specifies how the operation changes the Excise Stamp availability in the correspondent Box. The boxes are used to report the availability of excise stamps in the relevant locations according to the requirements of the customs administration. `Required` `Default("N")` 
| [Box3Effect](Finance.Excise.ExciseStampOperationTypes.md#box3effect) | [ExciseStampOperation<br />TypeEnum](Finance.Excise.ExciseStampOperationTypes.md#box3effect) | Specifies how the operation changes the Excise Stamp availability in the correspondent Box. The boxes are used to report the availability of excise stamps in the relevant locations according to the requirements of the customs administration. `Required` `Default("N")` 
| [Code](Finance.Excise.ExciseStampOperationTypes.md#code) | string (32) | The unique code of the ExciseStampOperationType. `Required` `Filter(multi eq)` 
| [DisplayText](Finance.Excise.ExciseStampOperationTypes.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [Id](Finance.Excise.ExciseStampOperationTypes.md#id) | guid |  
| [Name](Finance.Excise.ExciseStampOperationTypes.md#name) | [MultilanguageString (254)](../data-types.md#multilanguagestring) | Name of operation (multi-language string). `Required` `Filter(like)` 
| [ObjectVersion](Finance.Excise.ExciseStampOperationTypes.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 


## Attribute Details

### Box1Effect

Specifies how the operation changes the Excise Stamp availability in the correspondent Box. The boxes are used to report the availability of excise stamps in the relevant locations according to the requirements of the customs administration. `Required` `Default("N")`

_Type_: **[ExciseStampOperation<br />TypeEnum](Finance.Excise.ExciseStampOperationTypes.md#box1effect)**  
_Category_: **System**  
Generic enum type for ExciseStampOperationTypeEnum properties  
_Allowed Values (Finance.Excise.ExciseStampOperationTypeEnum Enum Members)_  

| Value | Description |
| ---- | --- |
| NoChange | Value is not changed. Stored as 'N'. <br /> _Database Value:_ 'N' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NoChange' |
| Plus | Add value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Plus' |
| Minus | Subtract value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Minus' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **NoChange**  

### Box2Effect

Specifies how the operation changes the Excise Stamp availability in the correspondent Box. The boxes are used to report the availability of excise stamps in the relevant locations according to the requirements of the customs administration. `Required` `Default("N")`

_Type_: **[ExciseStampOperation<br />TypeEnum](Finance.Excise.ExciseStampOperationTypes.md#box2effect)**  
_Category_: **System**  
Generic enum type for ExciseStampOperationTypeEnum properties  
_Allowed Values (Finance.Excise.ExciseStampOperationTypeEnum Enum Members)_  

| Value | Description |
| ---- | --- |
| NoChange | Value is not changed. Stored as 'N'. <br /> _Database Value:_ 'N' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NoChange' |
| Plus | Add value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Plus' |
| Minus | Subtract value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Minus' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **NoChange**  

### Box3Effect

Specifies how the operation changes the Excise Stamp availability in the correspondent Box. The boxes are used to report the availability of excise stamps in the relevant locations according to the requirements of the customs administration. `Required` `Default("N")`

_Type_: **[ExciseStampOperation<br />TypeEnum](Finance.Excise.ExciseStampOperationTypes.md#box3effect)**  
_Category_: **System**  
Generic enum type for ExciseStampOperationTypeEnum properties  
_Allowed Values (Finance.Excise.ExciseStampOperationTypeEnum Enum Members)_  

| Value | Description |
| ---- | --- |
| NoChange | Value is not changed. Stored as 'N'. <br /> _Database Value:_ 'N' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NoChange' |
| Plus | Add value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Plus' |
| Minus | Subtract value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Minus' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **NoChange**  

### Code

The unique code of the ExciseStampOperationType. `Required` `Filter(multi eq)`

_Type_: **string (32)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of operation (multi-language string). `Required` `Filter(like)`

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

[!list limit=1000 erp.entity=Finance.Excise.ExciseStampOperationTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExciseStampOperationTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Excise_ExciseStampOperationTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Excise_ExciseStampOperationTypes?$top=10>

