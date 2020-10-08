---
uid: Crm.Pos.Terminals
---
# Crm.Pos.Terminals

Represents a POS workplace for 1 person, with all the attached devices. (Not to be confused with Payment Terminal, which is specific POS device). Entity: Pos_Terminals (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Pos.Terminals.md#Id) | guid |  
| [IsActive](Crm.Pos.Terminals.md#IsActive) | boolean | Represents whether the POS terminal is active and can be chosen from drop-downs for new records. [Required] [Default(true)] [Filter(multi eq)] 
| [PosTerminalCode](Crm.Pos.Terminals.md#PosTerminalCode) | string | Unique (within the location) code of the POS terminal. [Required] [Filter(eq;like)] 
| [PosTerminalName](Crm.Pos.Terminals.md#PosTerminalName) | [MultilanguageString](../data-types.md#MultilanguageString) | The multi-language name of the terminal, like "Cash 1", "Self-checkout 5", etc. [Required] [Filter(multi eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultFiscalPrinterPosDevice](Crm.Pos.Terminals.md#DefaultFiscalPrinterPosDevice) | [Crm.Pos.Devices](Crm.Pos.Devices.md) (nullable) | The POS Fiscal Device which is set by default in documents when the POS Terminal is selected. [Filter(multi eq)] (Introduced in version 20.1.100.0) |
| [PosLocation](Crm.Pos.Terminals.md#PosLocation) | [Crm.Pos.Locations](Crm.Pos.Locations.md) | The POS location, where the terminal is located. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Devices | [Crm.Pos.Devices](Crm.Pos.Devices.md) | List of [Device](Crm.Pos.Devices.md) child objects, based on the [Crm.Pos.Device.PosTerminal](Crm.Pos.Devices.md#PosTerminal) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### IsActive

> Represents whether the POS terminal is active and can be chosen from drop-downs for new records. [Required] [Default(true)] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### PosTerminalCode

> Unique (within the location) code of the POS terminal. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### PosTerminalName

> The multi-language name of the terminal, like "Cash 1", "Self-checkout 5", etc. [Required] [Filter(multi eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### DefaultFiscalPrinterPosDevice

> The POS Fiscal Device which is set by default in documents when the POS Terminal is selected. [Filter(multi eq)] (Introduced in version 20.1.100.0)

_Type_: **[Crm.Pos.Devices](Crm.Pos.Devices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PosLocation

> The POS location, where the terminal is located. [Required] [Filter(multi eq)]

_Type_: **[Crm.Pos.Locations](Crm.Pos.Locations.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Pos.Terminals erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Pos.Terminals erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Pos.Terminals erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pos_Terminals?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pos_Terminals?$top=10>

