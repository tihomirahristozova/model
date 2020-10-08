---
uid: Systems.Core.DataEntryDefaultValues
---
# Systems.Core.DataEntryDefaultValues

Contains user-specified default values for columns in data entry forms. Entity: Sys_Default_Values

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.DataEntryDefaultValues.md#Id) | guid |  
| [ColumnName](Systems.Core.DataEntryDefaultValues.md#ColumnName) | string | The column for which the default is specified. [Required] [Filter(eq)] 
| [ConditionFormName](Systems.Core.DataEntryDefaultValues.md#ConditionFormName) | string (nullable) | If not null specifies that the default should be applied only if Form_Name equals the specified value. [Filter(eq)] [ORD] 
| [ConditionUserLogin](Systems.Core.DataEntryDefaultValues.md#ConditionUserLogin) | string (nullable) | If not null specifies that the default should be applied only if User_Login equals this value. [Filter(eq)] 
| [ConditionUserMachine](Systems.Core.DataEntryDefaultValues.md#ConditionUserMachine) | string (nullable) | If not null specifies that the default should be applied only if User_Machine equals this value. [Filter(eq)] 
| [DefaultValueField](Systems.Core.DataEntryDefaultValues.md#DefaultValueField) | string (nullable) | The default value for Column_Name. Should be applied only if the other conditions are met. null specifies null default. 
| [PanelName](Systems.Core.DataEntryDefaultValues.md#PanelName) | string (nullable) | When not null, specifies the panel for which the default value applies. [Filter(eq;like)] 
| [TableName](Systems.Core.DataEntryDefaultValues.md#TableName) | string (nullable) | The table, containing the column for which the default value is specified. [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ConditionDocumentType](Systems.Core.DataEntryDefaultValues.md#ConditionDocumentType) | [General.DocumentTypes](General.DocumentTypes.md) (nullable) | If not null specifies that the default should be applied only if Document_Type_Id equals this value. [Filter(multi eq)] |
| [ConditionEnterpriseCompany](Systems.Core.DataEntryDefaultValues.md#ConditionEnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | If not null specifies that the default should be applied only if Enterprise_Company_Id equals this value. [Filter(multi eq)] |
| [ConditionRole](Systems.Core.DataEntryDefaultValues.md#ConditionRole) | [Systems.Workflow.Roles](Systems.Workflow.Roles.md) (nullable) | When not null, specifies that the default value should be applied only when the user plays the specified role. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ColumnName

> The column for which the default is specified. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ConditionFormName

> If not null specifies that the default should be applied only if Form_Name equals the specified value. [Filter(eq)] [ORD]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### ConditionUserLogin

> If not null specifies that the default should be applied only if User_Login equals this value. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ConditionUserMachine

> If not null specifies that the default should be applied only if User_Machine equals this value. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### DefaultValueField

> The default value for Column_Name. Should be applied only if the other conditions are met. null specifies null default.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PanelName

> When not null, specifies the panel for which the default value applies. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### TableName

> The table, containing the column for which the default value is specified. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  


## Reference Details

### ConditionDocumentType

> If not null specifies that the default should be applied only if Document_Type_Id equals this value. [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ConditionEnterpriseCompany

> If not null specifies that the default should be applied only if Enterprise_Company_Id equals this value. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ConditionRole

> When not null, specifies that the default value should be applied only when the user plays the specified role. [Filter(multi eq)]

_Type_: **[Systems.Workflow.Roles](Systems.Workflow.Roles.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Core.DataEntryDefaultValues erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.DataEntryDefaultValues erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Core.DataEntryDefaultValues erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_DataEntryDefaultValues?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_DataEntryDefaultValues?$top=10>

