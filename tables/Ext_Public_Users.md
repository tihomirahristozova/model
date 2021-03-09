# Table Ext_Public_Users

/Users of the publicly offered services. This includes Internet, external and employee users. Entity: Ext_Public_Users

## Summary

| Name | Type | Description |
| - | - | --- |
|[Public_User_Id](#public_user_id)|`uniqueidentifier` `PK`||
|[Public_User_List_Id](#public_user_list_id)|`uniqueidentifier` |The list in which the user account is saved.|
|[First_Name](#first_name)|`nvarchar(64)` |First name of the user.|
|[Last_Name](#last_name)|`nvarchar(64)` |Last name of the user.|
|[Password_Algorithm](#password_algorithm)|`nvarchar(16)` |Uniquely specifies the password storage algorithm among some system recognized algorithms. Usually specifies the hashing and the stretching functions. For example, 'PBKDF2-SHA1'.|
|[Password_Hash](#password_hash)|`nvarchar(128)` |Actual password storage. The format of the contents is determined by Password Algorithm.|
|[Is_Active](#is_active)|`bit` |Specifies whether the user account is active and access should be allowed.|
|[Email](#email)|`nvarchar(64)` |The primary email of the user. Used for notifications and password restore.|
|[Alternate_Email](#alternate_email)|`nvarchar(64)` |Alternate email of the user. Can be used for backup email for password restore.|
|[Country](#country)|`nvarchar(64)` |The country of residence of the user, with latin letters.|
|[State](#state)|`nvarchar(64)` |The state of residence of the user within the country. Can be specified with latin or local characters.|
|[City](#city)|`nvarchar(64)` |The state of residence of the user. Can be specified with latin or local letters.|
|[Address](#address)|`nvarchar(128)` |The primary address of the user. Can be specified with latin or local characters.|
|[Postal_Code](#postal_code)|`nvarchar(16)` |The postal code of the default address of the user.|
|[Phone_Number](#phone_number)|`nvarchar(16)` |The primary phone number of the user.|
|[Company_Name](#company_name)|`nvarchar(64)` |The name of the company, for which the user works, as specified by the user.|
|[Company_Id](#company_id)|`uniqueidentifier` |Link to an internal company record, specified by internal employee.|
|[Person_Id](#person_id)|`uniqueidentifier` |Link to an internal person record. Usually specified by internal employee, but can also be an automated process.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Profile_Picture](#profile_picture)|`varbinary` |Profile picture of the user.|
|[About_Me_Text](#about_me_text)|`nvarchar(1024)` |About me text, written by the user.|
|[Created_On](#created_on)|`datetime` |The date and time when the user was created.|
|[Password_Recovery_Code](#password_recovery_code)|`uniqueidentifier` Readonly||
|[Password_Recovery_Creation_Time](#password_recovery_creation_time)|`datetime` Readonly||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Public_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Public_User_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### First_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Last_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Password_Algorithm

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Password_Hash

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Email

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Alternate_Email

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Country

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### State

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### City

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Address

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Postal_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Phone_Number

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Company_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Profile_Picture

| Property | Value |
| - | - |
|Type|varbinary|

### About_Me_Text

| Property | Value |
| - | - |
|Type|nvarchar(1024)|

### Created_On

| Property | Value |
| - | - |
|Type|datetime|

### Password_Recovery_Code

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Password_Recovery_Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


