# Query Pdm_Processing_Consents_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Processing_Consent_Id](#processing_consent_id)|`uniqueidentifier` `PK`||
|[Person_Id](#person_id)|`uniqueidentifier` |The person, for which the consent is given. Null when the consent is given by an online user, which is still not linked to a specific person record.|
|[User_Id](#user_id)|`uniqueidentifier` |The login user, for which the consent is given. Null when a consent is entered for a natural person, not through online user.|
|[Personal_Data_Process_Id](#personal_data_process_id)|`uniqueidentifier` |The process, which will be used to process the data. Null when the process is unknown, or there are multiple processes (not recommended) processing the data, listed in the Notes.|
|[Given_On_Utc](#given_on_utc)|`datetime` |The date and time (in Utc), when the consent was given.|
|[Retracted_On_Utc](#retracted_on_utc)|`datetime` |The date and time (in Utc), when the consent was retracted. Null if the consent is not retracted.|
|[Is_Active](#is_active)|`bit` |Whether the consent is active or retracted. Once retracted, the consent record cannot be modified again and a new consent should be given.|
|[Is_Child](#is_child)|`bit` |Specifies whether the data subject is child, according to the local regulations. General regulations treat all persons below the age of 16 as child.|
|[Parent_Name](#parent_name)|`nvarchar` |When a parental rights holder gives a consent for a child, contains the name of the parent.|
|[Parent_Email](#parent_email)|`nvarchar` |When a parental rights holder gives a consent for a child, contains the email of the parent.|
|[Parent_Phone](#parent_phone)|`nvarchar` |When a parental rights holder gives a consent for a child, contains the phone number of the parent.|
|[Consent_Type](#consent_type)|`nvarchar` Allowed: `O`, `I`, `V`, `W`, `E`, `T`|The way the consent was given. O=Online; I=Implicit; V=Verbal; W=Written; E=Email; T=Other (should be stated in Notes).|
|[Consent_Text](#consent_text)|`nvarchar` |The actual text of the consent.|
|[Consent_Image](#consent_image)|`varbinary` |If not null, it is a graphical image, containing additional information for the consent.|
|[Allow_Basic_Data](#allow_basic_data)|`bit` |Allows the processing of basic (usually public) data: Name, AgeGroup21+, public profile picture, etc.|
|[Allow_Email](#allow_email)|`bit` |Allows the processing of the email address.|
|[Allow_Address](#allow_address)|`bit` |Allows the processing of the physical address.|
|[Allow_Phone](#allow_phone)|`bit` |Allows the processing of the telephone number.|
|[Allow_Other_Data](#allow_other_data)|`nvarchar` |Comma-separated list of other types of data, which was allowed for processing with this consent.|
|[Notes](#notes)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Processing_Consent_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Personal_Data_Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Given_On_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Retracted_On_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Is_Child

| Property | Value |
| - | - |
|Type|bit|

### Parent_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Email

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Phone

| Property | Value |
| - | - |
|Type|nvarchar|

### Consent_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Consent_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Consent_Image

| Property | Value |
| - | - |
|Type|varbinary|

### Allow_Basic_Data

| Property | Value |
| - | - |
|Type|bit|

### Allow_Email

| Property | Value |
| - | - |
|Type|bit|

### Allow_Address

| Property | Value |
| - | - |
|Type|bit|

### Allow_Phone

| Property | Value |
| - | - |
|Type|bit|

### Allow_Other_Data

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


