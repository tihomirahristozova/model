# Table Cm_Contact_Mechanisms

Contains contacting mechanisms - telephone numbers, addresses, web sites, etc. Contact mechanisms can be attached to parties. Currently each contact mechanism is attached to strictly one party. Entity: Cm_Contact_Mechanisms

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Contact_Mechanism_Type|`ContactMechanismType`|Allowed: `A`, `E`, `F`, `M`, `O`, `T`, `W`|A=Address; E=e-mail; T=Telephone. `Required` `Default("A")` `Filter(multi eq)` |
|Contact_Mechanism_Name|`String`||Contact mechanism description. `Required` `Filter(eq;like)` |
