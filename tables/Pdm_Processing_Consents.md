# Table Pdm_Processing_Consents

Consents of data subjects for processing of their personal data. Entity: Pdm_Processing_Consents (Introduced in version 18.2)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Processing_Consent_Id|`Guid`|`PK`, Readonly||
|Allow_Address|`Boolean`||Allows the processing of the physical address. `Required` `Default(false)` `Filter(eq)` |
|Allow_Basic_Data|`Boolean`||Allows the processing of basic (usually public) data: Name, AgeGroup21+, public profile picture, etc. `Required` `Default(false)` `Filter(eq)` |
|Allow_Email|`Boolean`||Allows the processing of the email address. `Required` `Default(false)` `Filter(eq)` |
|Allow_Other_Data|`String`||Comma-separated list of other types of data, which was allowed for processing with this consent. `Filter(eq)` |
|Allow_Phone|`Boolean`||Allows the processing of the telephone number. `Required` `Default(false)` `Filter(eq)` |
|Consent_Image|`Byte[]`|`BLOB`|If not null, it is a graphical image, containing additional information for the consent. |
|Consent_Text|`String`||The actual text of the consent. `Filter(like)` |
|Consent_Type|`ConsentType`|Allowed: `O`, `I`, `V`, `W`, `E`, `T`|The way the consent was given. O=Online; I=Implicit; V=Verbal; W=Written; E=Email; T=Other (should be stated in Notes). `Required` `Filter(eq)` |
|Given_On_Utc|`DateTime`||The date and time (in Utc), when the consent was given. `Required` `Filter(ge;le)` |
|Is_Active|`Boolean`||Whether the consent is active or retracted. Once retracted, the consent record cannot be modified again and a new consent should be given. `Required` `Default(true)` `Filter(eq)` |
|Is_Child|`Boolean`||Specifies whether the data subject is child, according to the local regulations. General regulations treat all persons below the age of 16 as child. `Required` `Default(false)` `Filter(eq)` |
|Notes|`String`||Notes for this ProcessingConsent. |
|Parent_Email|`String`||When a parental rights holder gives a consent for a child, contains the email of the parent. `Filter(like)` |
|Parent_Name|`String`||When a parental rights holder gives a consent for a child, contains the name of the parent. `Filter(eq;like)` |
|Parent_Phone|`String`||When a parental rights holder gives a consent for a child, contains the phone number of the parent. `Filter(like)` |
|Retracted_On_Utc|`DateTime?`||The date and time (in Utc), when the consent was retracted. Null if the consent is not retracted. `Filter(ge;le)` |
