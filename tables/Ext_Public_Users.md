# Table Ext_Public_Users

/Users of the publicly offered services. This includes Internet, external and employee users. Entity: Ext_Public_Users

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Public_User_Id|`Guid`|`PK`, Readonly||
|About_Me_Text|`String`||About me text, written by the user. |
|Address|`String`||The primary address of the user. Can be specified with latin or local characters. `Filter(like)` |
|Alternate_Email|`String`||Alternate email of the user. Can be used for backup email for password restore. `Filter(like)` |
|City|`String`||The state of residence of the user. Can be specified with latin or local letters. `Filter(like)` |
|Company_Name|`String`||The name of the company, for which the user works, as specified by the user. `Filter(like)` |
|Country|`String`||The country of residence of the user, with latin letters. `Filter(like)` |
|Created_On|`DateTime?`||The date and time when the user was created. `Default(Now)` |
|Email|`String`||The primary email of the user. Used for notifications and password restore. `Required` `Filter(like)` |
|First_Name|`String`||First name of the user. `Required` `Filter(like)` |
|Is_Active|`Boolean`||Specifies whether the user account is active and access should be allowed. `Required` `Default(true)` `Filter(eq)` |
|Last_Name|`String`||Last name of the user. `Required` `Filter(like)` |
|Notes|`String`||Notes for this PublicUser. |
|Password_Algorithm|`String`||Uniquely specifies the password storage algorithm among some system recognized algorithms. Usually specifies the hashing and the stretching functions. For example, 'PBKDF2-SHA1'. `Required` `Filter(like)` |
|Password_Hash|`String`||Actual password storage. The format of the contents is determined by Password Algorithm. `Required` `Filter(like)` |
|Password_Recovery_Code|`Guid?`|Readonly|Automatically generated unique code for the last password recovery attempt. `Filter(multi eq)` `ReadOnly` |
|Password_Recovery_Creation_Time|`DateTime?`|Readonly|Date and time when the last password recovery code was created. `ReadOnly` |
|Phone_Number|`String`||The primary phone number of the user. `Filter(like)` |
|Postal_Code|`String`||The postal code of the default address of the user. `Filter(like)` |
|Profile_Picture|`Byte[]`|`BLOB`|Profile picture of the user. |
|State|`String`||The state of residence of the user within the country. Can be specified with latin or local characters. `Filter(like)` |
