---
uid: Systems.Security.ColumnPermissions
---
# Systems.Security.ColumnPermissions

User permissions for accessing the system data columns. Entity: Sec_Column_Permissions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.ColumnPermissions.md#Id) | guid |  
| [ColumnName](Systems.Security.ColumnPermissions.md#ColumnName) | string | The name of the secured column. [Required] [Filter(eq)] 
| [TableName](Systems.Security.ColumnPermissions.md#TableName) | string | The table in which is the secured column. [Required] [Filter(eq)] [ORD] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.Security.ColumnPermissions.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The required access key for accessing the column. [Filter(multi eq)] [ReadOnly] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ColumnName

> The name of the secured column. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### TableName

> The table in which is the secured column. [Required] [Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  


## Reference Details

### AccessKey

> The required access key for accessing the column. [Filter(multi eq)] [ReadOnly]

_Type_: **[Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Security.ColumnPermissions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.ColumnPermissions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Security.ColumnPermissions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_ColumnPermissions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_ColumnPermissions?$top=10>

