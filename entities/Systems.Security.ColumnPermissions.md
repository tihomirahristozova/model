---
uid: Systems.Security.ColumnPermissions
---
# Systems.Security.ColumnPermissions Entity

**Namespace:** [Systems.Security](Systems.Security.md)  

User permissions for accessing the system data columns. Entity: Sec_Column_Permissions

## Default Visualization
Default Display Text Format:  
_{ColumnName}_  
Default Search Members:  
_ColumnName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Security.ColumnPermissions](Systems.Security.ColumnPermissions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ColumnName](Systems.Security.ColumnPermissions.md#columnname) | string (128) | The name of the secured column. `Required` `Filter(eq)` 
| [Id](Systems.Security.ColumnPermissions.md#id) | guid |  
| [ObjectVersion](Systems.Security.ColumnPermissions.md#objectversion) | int32 |  
| [TableName](Systems.Security.ColumnPermissions.md#tablename) | string (128) | The table in which is the secured column. `Required` `Filter(eq)` `ORD` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.Security.ColumnPermissions.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The required access key for accessing the column. `Filter(multi eq)` `ReadOnly` |


## Attribute Details

### ColumnName

The name of the secured column. `Required` `Filter(eq)`

_Type_: **string (128)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### TableName

The table in which is the secured column. `Required` `Filter(eq)` `ORD`

_Type_: **string (128)**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Maximum Length_: **128**  


## Reference Details

### AccessKey

The required access key for accessing the column. `Filter(multi eq)` `ReadOnly`

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources does not support ordering.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description  
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

[!list limit=1000 erp.entity=Systems.Security.ColumnPermissions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Security.ColumnPermissions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_ColumnPermissions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_ColumnPermissions?$top=10>

