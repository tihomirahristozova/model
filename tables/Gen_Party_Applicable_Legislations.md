# Table Gen_Party_Applicable_Legislations

Specifies a legislation, which is applicable for a party. A single party can have more than one applicable legislations. Entity: Gen_Party_Applicable_Legislations (Introduced in version 19.1)

# Aggregate Hierarchy

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Party_Applicable_Legislation_Id|`Guid`|`PK`, Readonly||
|Applicable_Legislation|`ApplicableLegislation`|Allowed: `AE`, `AU`, `BG`, `CA`, `CN`, `CZ`, `DE`, `ES`, `EU`, `FR`, `GR`, `HU`, `IN`, `IT`, `JP`, `MK`, `PL`, `PT`, `RO`, `RS`, `RU`, `TR`, `UK`, `US`, `ZA`|A legislation, which applies to the specified party. The list of legislations is system defined, and contains legislations for which system rules are currently defined. For example: US, UK, EU, DE, FR, ES, IT, BG, MK, RO, GR, etc. `Required` `Filter(multi eq)` `ORD` |
|Notes|`String`||Notes for this PartyApplicableLegislation. `Filter(like)` |
