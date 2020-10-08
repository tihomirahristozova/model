---
uid: Crm.Pos.Devices
---
# Crm.Pos.Devices

Represents one POS device, attached to a POS terminal. Entity: Pos_Devices (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Pos.Devices.md#Id) | guid |  
| [DeviceRegistrationNo](Crm.Pos.Devices.md#DeviceRegistrationNo) | string (nullable) | The unique registration number of the device, assigned by the manufacturer. null means the number is unknown or N/A. [Filter(multi eq;like)] 
| [DeviceType](Crm.Pos.Devices.md#DeviceType) | [Crm.Pos.DevicesRepository.DeviceType](Crm.Pos.Devices.md#DeviceType) | Type of the POS device. PAY=Payment Terminal; CSH=Cash Drawer; FIP=Fiscal Printer; OTH=Other. [Required] [Default("OTH")] [Filter(multi eq)] 
| [ElectronicAddress](Crm.Pos.Devices.md#ElectronicAddress) | string (nullable) | The absolute address (Internet or other) which can be used for electronic communication with the device. The address should contain communication protocol/type, colon, space, then the actual address. Addresses, which are local to a specific computer, should also include the computer name. For example: "COM: PC_WORK1:COM1", "HTTP: https://<addr>", etc. [Filter(multi eq;like)] 
| [IsActive](Crm.Pos.Devices.md#IsActive) | boolean | Indicates whether the device is currently active and can be choosen from drop-downs in new records. [Required] [Default(true)] [Filter(multi eq)] 
| [ProtocolName](Crm.Pos.Devices.md#ProtocolName) | [Crm.Pos.DevicesRepository.ProtocolName](Crm.Pos.Devices.md#ProtocolName) (nullable) | The name of the protocol, which can be used to communicate with the device. null means that the protocol is unknown and programmatic communication with the device would not be performed. 
| [SettingsJson](Crm.Pos.Devices.md#SettingsJson) | string (nullable) | Settings and operator access codes for the POS device. The data is stored as Json, encrypted for the current application server instance. null means that there are no settings for this device. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PosTerminal](Crm.Pos.Devices.md#PosTerminal) | [Crm.Pos.Terminals](Crm.Pos.Terminals.md) | The POS terminal, to which this device is attached. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DeviceRegistrationNo

> The unique registration number of the device, assigned by the manufacturer. null means the number is unknown or N/A. [Filter(multi eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### DeviceType

> Type of the POS device. PAY=Payment Terminal; CSH=Cash Drawer; FIP=Fiscal Printer; OTH=Other. [Required] [Default("OTH")] [Filter(multi eq)]

_Type_: **[Crm.Pos.DevicesRepository.DeviceType](Crm.Pos.Devices.md#DeviceType)**  
Allowed values for the [DeviceType](Crm.Pos.Devices.md#DeviceType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| PaymentTerminal | PaymentTerminal value. Stored as 'PAY'. <br /> _Database Value:_ 'PAY' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'PaymentTerminal' |
| CashDrawer | CashDrawer value. Stored as 'CSH'. <br /> _Database Value:_ 'CSH' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'CashDrawer' |
| FiscalPrinter | FiscalPrinter value. Stored as 'FIP'. <br /> _Database Value:_ 'FIP' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'FiscalPrinter' |
| Other | Other value. Stored as 'OTH'. <br /> _Database Value:_ 'OTH' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Other' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **Other**  

### ElectronicAddress

> The absolute address (Internet or other) which can be used for electronic communication with the device. The address should contain communication protocol/type, colon, space, then the actual address. Addresses, which are local to a specific computer, should also include the computer name. For example: "COM: PC_WORK1:COM1", "HTTP: https://<addr>", etc. [Filter(multi eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### IsActive

> Indicates whether the device is currently active and can be choosen from drop-downs in new records. [Required] [Default(true)] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### ProtocolName

> The name of the protocol, which can be used to communicate with the device. null means that the protocol is unknown and programmatic communication with the device would not be performed.

_Type_: **[Crm.Pos.DevicesRepository.ProtocolName](Crm.Pos.Devices.md#ProtocolName) (nullable)**  
Allowed values for the [ProtocolName](Crm.Pos.Devices.md#ProtocolName) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| ERPNETFP | ERPNETFP value. Stored as 'ERPNET_FP'. <br /> _Database Value:_ 'ERPNET_FP' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'ERPNETFP' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SettingsJson

> Settings and operator access codes for the POS device. The data is stored as Json, encrypted for the current application server instance. null means that there are no settings for this device.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### PosTerminal

> The POS terminal, to which this device is attached. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Crm.Pos.Terminals](Crm.Pos.Terminals.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Pos.Devices erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Pos.Devices erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Pos.Devices erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pos_Devices?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pos_Devices?$top=10>

