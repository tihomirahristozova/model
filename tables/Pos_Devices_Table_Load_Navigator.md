# Query Pos_Devices_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Pos_Device_Id](#pos_device_id)|`uniqueidentifier` `PK`||
|[Pos_Terminal_Id](#pos_terminal_id)|`uniqueidentifier` |The POS terminal, to which this device is attached.|
|[Device_Type](#device_type)|`nvarchar` Allowed: `PAY`, `CSH`, `FIP`, `OTH`|Type of the POS device. PAY=Payment Terminal; CSH=Cash Drawer; FIP=Fiscal Printer; OTH=Other.|
|[Device_Registration_No](#device_registration_no)|`nvarchar` |The unique registration number of the device, assigned by the manufacturer. NULL means the number is unknown or N/A.|
|[Protocol_Name](#protocol_name)|`nvarchar` Allowed: `ERPNET_FP`|The name of the protocol, which can be used to communicate with the device. NULL means that the protocol is unknown and programmatic communication with the device would not be performed.|
|[Electronic_Address](#electronic_address)|`nvarchar` |The absolute address (Internet or other) which can be used for electronic communication with the device. The address should contain communication protocol/type, colon, space, then the actual address. Addresses, which are local to a specific computer, should also include the computer name. For example: "COM: PC_WORK1:COM1", "HTTP: https://<addr>", etc.|
|[Settings_Json](#settings_json)|`nvarchar` |Settings and operator access codes for the POS device. The data is stored as Json, encrypted for the current application server instance. NULL means that there are no settings for this device.|
|[Is_Active](#is_active)|`bit` |Indicates whether the device is currently active and can be choosen from drop-downs in new records.|
|[Pos_Location_Id](#pos_location_id)|`uniqueidentifier` ||
|[Pos_Terminal_Code](#pos_terminal_code)|`nvarchar` |Unique (within the location) code of the POS terminal.|
|[Pos_Terminal_Name](#pos_terminal_name)|`nvarchar` `ML`|The multi-language name of the terminal, like "Cash 1", "Self-checkout 5", etc.|
|[Pos_Terminal_Is_Active](#pos_terminal_is_active)|`bit` |Represents whether the POS terminal is active and can be chosen from drop-downs for new records.|
|[Default_Fiscal_Printer_Pos_Device_Id](#default_fiscal_printer_pos_device_id)|`uniqueidentifier` |The POS Fiscal Device which is set by default in documents when the POS Terminal is selected.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company of the POS location.|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location of the POS location. Currently, only one POS location is allowed for each company location.|
|[Pos_Location_Code](#pos_location_code)|`nvarchar` |Unique (with the enterprise company) code of this POS location.|
|[Pos_Location_Is_Active](#pos_location_is_active)|`bit` |Indicates whether the POS location is currently active and can be chosen in drop-downs, etc.|

## Columns

### Pos_Device_Id


Pos_Device_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Pos_Devices](Pos_Devices.md).[Pos_Device_Id](Pos_Devices.md#pos_device_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Pos_Terminal_Id


Pos_Terminal_Id


The POS terminal, to which this device is attached.


The POS terminal, to which this device is attached.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Pos_Terminals](Pos_Terminals.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pos_Devices](Pos_Devices.md).[Pos_Terminal_Id](Pos_Devices.md#pos_terminal_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Device_Type


Device_Type


Type of the POS device. PAY=Payment Terminal; CSH=Cash Drawer; FIP=Fiscal Printer; OTH=Other.


Type of the POS device. PAY=Payment Terminal; CSH=Cash Drawer; FIP=Fiscal Printer; OTH=Other.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`PAY`, `CSH`, `FIP`, `OTH`|
|Default Value|OTH|
|Derived From|[Pos_Devices](Pos_Devices.md).[Device_Type](Pos_Devices.md#device_type)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Device_Registration_No


Device_Registration_No


The unique registration number of the device, assigned by the manufacturer. NULL means the number is unknown or N/A.


The unique registration number of the device, assigned by the manufacturer. NULL means the number is unknown or N/A.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pos_Devices](Pos_Devices.md).[Device_Registration_No](Pos_Devices.md#device_registration_no)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Protocol_Name


Protocol_Name


The name of the protocol, which can be used to communicate with the device. NULL means that the protocol is unknown and programmatic communication with the device would not be performed.


The name of the protocol, which can be used to communicate with the device. NULL means that the protocol is unknown and programmatic communication with the device would not be performed.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`ERPNET_FP`|
|Default Value|None|
|Derived From|[Pos_Devices](Pos_Devices.md).[Protocol_Name](Pos_Devices.md#protocol_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Electronic_Address


Electronic_Address


The absolute address (Internet or other) which can be used for electronic communication with the device. The address should contain communication protocol/type, colon, space, then the actual address. Addresses, which are local to a specific computer, should also include the computer name. For example: "COM: PC_WORK1:COM1", "HTTP: https://<addr>", etc.


The absolute address (Internet or other) which can be used for electronic communication with the device. The address should contain communication protocol/type, colon, space, then the actual address. Addresses, which are local to a specific computer, should also include the computer name. For example: "COM: PC_WORK1:COM1", "HTTP: https://<addr>", etc.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pos_Devices](Pos_Devices.md).[Electronic_Address](Pos_Devices.md#electronic_address)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Settings_Json


Settings_Json


Settings and operator access codes for the POS device. The data is stored as Json, encrypted for the current application server instance. NULL means that there are no settings for this device.


Settings and operator access codes for the POS device. The data is stored as Json, encrypted for the current application server instance. NULL means that there are no settings for this device.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pos_Devices](Pos_Devices.md).[Settings_Json](Pos_Devices.md#settings_json)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Active


Is_Active


Indicates whether the device is currently active and can be choosen from drop-downs in new records.


Indicates whether the device is currently active and can be choosen from drop-downs in new records.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Pos_Devices](Pos_Devices.md).[Is_Active](Pos_Devices.md#is_active)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Pos_Location_Id


Pos_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Pos_Locations](Pos_Locations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pos_Terminals](Pos_Terminals.md).[Pos_Location_Id](Pos_Terminals.md#pos_location_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Pos_Terminal_Code


Pos_Terminal_Code


Unique (within the location) code of the POS terminal.


Unique (within the location) code of the POS terminal.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pos_Terminals](Pos_Terminals.md).[Pos_Terminal_Code](Pos_Terminals.md#pos_terminal_code)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Pos_Terminal_Name


Pos_Terminal_Name


The multi-language name of the terminal, like "Cash 1", "Self-checkout 5", etc.


The multi-language name of the terminal, like "Cash 1", "Self-checkout 5", etc.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pos_Terminals](Pos_Terminals.md).[Pos_Terminal_Name](Pos_Terminals.md#pos_terminal_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Pos_Terminal_Is_Active


Pos_Terminal_Is_Active


Represents whether the POS terminal is active and can be chosen from drop-downs for new records.


Represents whether the POS terminal is active and can be chosen from drop-downs for new records.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Pos_Terminals](Pos_Terminals.md).[Is_Active](Pos_Terminals.md#is_active)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Default_Fiscal_Printer_Pos_Device_Id


Default_Fiscal_Printer_Pos_Device_Id


The POS Fiscal Device which is set by default in documents when the POS Terminal is selected.


The POS Fiscal Device which is set by default in documents when the POS Terminal is selected.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Pos_Devices](Pos_Devices.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pos_Terminals](Pos_Terminals.md).[Default_Fiscal_Printer_Pos_Device_Id](Pos_Terminals.md#default_fiscal_printer_pos_device_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Enterprise_Company_Id


Enterprise_Company_Id


The enterprise company of the POS location.


The enterprise company of the POS location.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pos_Locations](Pos_Locations.md).[Enterprise_Company_Id](Pos_Locations.md#enterprise_company_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Enterprise_Company_Location_Id


Enterprise_Company_Location_Id


The enterprise company location of the POS location. Currently, only one POS location is allowed for each company location.


The enterprise company location of the POS location. Currently, only one POS location is allowed for each company location.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Company_Locations](Cm_Company_Locations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pos_Locations](Pos_Locations.md).[Enterprise_Company_Location_Id](Pos_Locations.md#enterprise_company_location_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|14|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Pos_Location_Code


Pos_Location_Code


Unique (with the enterprise company) code of this POS location.


Unique (with the enterprise company) code of this POS location.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pos_Locations](Pos_Locations.md).[Pos_Location_Code](Pos_Locations.md#pos_location_code)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|15|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Pos_Location_Is_Active


Pos_Location_Is_Active


Indicates whether the POS location is currently active and can be chosen in drop-downs, etc.


Indicates whether the POS location is currently active and can be chosen in drop-downs, etc.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Pos_Locations](Pos_Locations.md).[Is_Active](Pos_Locations.md#is_active)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|16|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|


