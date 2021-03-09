# Query Ext_Public_Users_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Public_User_Id](#public_user_id)|`uniqueidentifier` `PK`||
|[Public_User_List_Id](#public_user_list_id)|`uniqueidentifier` |The list in which the user account is saved.|
|[First_Name](#first_name)|`nvarchar` |First name of the user.|
|[Last_Name](#last_name)|`nvarchar` |Last name of the user.|
|[Password_Algorithm](#password_algorithm)|`nvarchar` |Uniquely specifies the password storage algorithm among some system recognized algorithms. Usually specifies the hashing and the stretching functions. For example, 'PBKDF2-SHA1'.|
|[Password_Hash](#password_hash)|`nvarchar` |Actual password storage. The format of the contents is determined by Password Algorithm.|
|[Is_Active](#is_active)|`bit` |Specifies whether the user account is active and access should be allowed.|
|[Email](#email)|`nvarchar` |The primary email of the user. Used for notifications and password restore.|
|[Alternate_Email](#alternate_email)|`nvarchar` |Alternate email of the user. Can be used for backup email for password restore.|
|[Country](#country)|`nvarchar` |The country of residence of the user, with latin letters.|
|[State](#state)|`nvarchar` |The state of residence of the user within the country. Can be specified with latin or local characters.|
|[City](#city)|`nvarchar` |The state of residence of the user. Can be specified with latin or local letters.|
|[Address](#address)|`nvarchar` |The primary address of the user. Can be specified with latin or local characters.|
|[Postal_Code](#postal_code)|`nvarchar` |The postal code of the default address of the user.|
|[Phone_Number](#phone_number)|`nvarchar` |The primary phone number of the user.|
|[Company_Name](#company_name)|`nvarchar` |The name of the company, for which the user works, as specified by the user.|
|[Company_Id](#company_id)|`uniqueidentifier` |Link to an internal company record, specified by internal employee.|
|[Person_Id](#person_id)|`uniqueidentifier` |Link to an internal person record. Usually specified by internal employee, but can also be an automated process.|
|[Notes](#notes)|`nvarchar` ||
|[Profile_Picture](#profile_picture)|`varbinary` |Profile picture of the user.|
|[About_Me_Text](#about_me_text)|`nvarchar` |About me text, written by the user.|
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
|Type|nvarchar|

### Last_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Password_Algorithm

| Property | Value |
| - | - |
|Type|nvarchar|

### Password_Hash

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Email

| Property | Value |
| - | - |
|Type|nvarchar|

### Alternate_Email

| Property | Value |
| - | - |
|Type|nvarchar|

### Country

| Property | Value |
| - | - |
|Type|nvarchar|

### State

| Property | Value |
| - | - |
|Type|nvarchar|

### City

| Property | Value |
| - | - |
|Type|nvarchar|

### Address

| Property | Value |
| - | - |
|Type|nvarchar|

### Postal_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Phone_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Company_Name

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Profile_Picture

| Property | Value |
| - | - |
|Type|varbinary|

### About_Me_Text

| Property | Value |
| - | - |
|Type|nvarchar|

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


