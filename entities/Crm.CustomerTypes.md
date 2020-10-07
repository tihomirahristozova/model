# Crm.CustomerTypes

User defined customer type. Primarily used for customer definition security, because it has record level security, which is also applied to the individual customer definitions. Entity: Crm_Customer_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.CustomerTypes.md#Id) | guid |  
| [Name](Crm.CustomerTypes.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | The name of this CustomerType. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Crm.CustomerTypes.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this CustomerType. Null means that all users have unlimited permissions. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Name

> The name of this CustomerType. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

> The access key, containing the user permissions for this CustomerType. Null means that all users have unlimited permissions. [Filter(multi eq)]

_Type_: **[Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.CustomerTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.CustomerTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.CustomerTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_CustomerTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_CustomerTypes?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Customer_Types?$top=10>

