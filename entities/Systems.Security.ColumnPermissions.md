---
uid: Systems.Security.ColumnPermissions
---
# Systems.Security.ColumnPermissions Entity

User permissions for accessing the system data columns. Entity: Sec_Column_Permissions

Default Display Text Format:  
_{ColumnName:T}_  
Default Search Member:  
_ColumnName_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ColumnName](Systems.Security.ColumnPermissions.md#columnname) | string | The name of the secured column. [Required] [Filter(eq)] 
| [Id](Systems.Security.ColumnPermissions.md#id) | guid |  
| [TableName](Systems.Security.ColumnPermissions.md#tablename) | string | The table in which is the secured column. [Required] [Filter(eq)] [ORD] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.Security.ColumnPermissions.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The required access key for accessing the column. [Filter(multi eq)] [ReadOnly] |


## Attribute Details

### ColumnName

The name of the secured column. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### TableName

The table in which is the secured column. [Required] [Filter(eq)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  


## Reference Details

### AccessKey

The required access key for accessing the column. [Filter(multi eq)] [ReadOnly]

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Security.ColumnPermissions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.ColumnPermissions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_ColumnPermissions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_ColumnPermissions?$top=10>

