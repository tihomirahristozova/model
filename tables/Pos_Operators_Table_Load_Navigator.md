# Query Pos_Operators_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Pos_Operator_Id](#pos_operator_id)|`uniqueidentifier` `PK`||
|[Pos_Location_Id](#pos_location_id)|`uniqueidentifier` |The POS location where this operator works.|
|[Pos_Operator_Code](#pos_operator_code)|`nvarchar` |Operator code. Unique within the Pos Location.|
|[User_Id](#user_id)|`uniqueidentifier` |The login user for this POS operator.|
|[Pos_Role_Id](#pos_role_id)|`uniqueidentifier` |The role, assigned to the operator. The role indicates the permissions of the operator for this POS location.|
|[Default_Pos_Terminal_Id](#default_pos_terminal_id)|`uniqueidentifier` |The default POS terminal for this opertor. NULL when there is no default.|
|[Starting_Date](#starting_date)|`date` |The first date, when the operator has started working for this POS location.|
|[Termination_Date](#termination_date)|`date` |The date, when the operator has ceased working in this POS location. NULL means, that the operator is still working or the termination date is still unknown.|
|[Is_Active](#is_active)|`bit` |Indicates whether this operator is active and can be chosen for new records.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location of the POS location. Currently, only one POS location is allowed for each company location.|
|[Pos_Location_Code](#pos_location_code)|`nvarchar` |Unique (with the enterprise company) code of this POS location.|
|[Pos_Location_Is_Active](#pos_location_is_active)|`bit` |Indicates whether the POS location is currently active and can be chosen in drop-downs, etc.|
|[Pos_Role_Code](#pos_role_code)|`nvarchar` |Unique role code.|
|[Pos_Role_Name](#pos_role_name)|`nvarchar` `ML`|Multi-language name of the POS role.|
|[Can_Void_Sales](#can_void_sales)|`bit` |Indicates whether this role can void sales orders.|
|[Can_Process_Minus_Sales](#can_process_minus_sales)|`bit` |Indicates whether the role is allowed to process minus (qty and/or value) sales.|
|[Person_Id](#person_id)|`uniqueidentifier` `PK`|Unique person Id|
|[Party_Id](#party_id)|`uniqueidentifier` |The Id of the party record for this person. The party stores the person's full name|
|[First_Name](#first_name)|`nvarchar` `ML`|First name of the person.|
|[Middle_Name](#middle_name)|`nvarchar` `ML`|Middle name of the person.|
|[Last_Name](#last_name)|`nvarchar` `ML`|Last name of the person.|
|[Title](#title)|`nvarchar` `ML`|The persons title. It may be one of the standard titles - Mr., Mrs., etc., but it can also contains professional or academic qualification.|
|[Gender](#gender)|`nvarchar` Allowed: `F`, `M`|Person gender. M=Male;F=Female;NULL=not known/not provided|
|[Birth_Date](#birth_date)|`datetime` |Birth date. NULL means unknown|
|[Nationality](#nationality)|`uniqueidentifier` |Person's nationality. NULL means the default (same as enterprise) nationality|
|[National_Number](#national_number)|`nvarchar` |Government assigned unique personal number. NULL means unknown|
|[Passport_Number](#passport_number)|`nvarchar` |Current passport number. NULL means unknown|
|[Passport_Issuing_Date](#passport_issuing_date)|`datetime` |Date of issuing the passport. NULL means unknown|
|[City](#city)|`nvarchar` `ML`|City from the legal registration address for the person|
|[Notes](#notes)|`nvarchar` |Internal notes for the person|
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar` Readonly||

## Columns

### Pos_Operator_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Operator_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Role_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Pos_Terminal_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Starting_Date

| Property | Value |
| - | - |
|Type|date|

### Termination_Date

| Property | Value |
| - | - |
|Type|date|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Location_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Pos_Location_Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Pos_Role_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Pos_Role_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Can_Void_Sales

| Property | Value |
| - | - |
|Type|bit|

### Can_Process_Minus_Sales

| Property | Value |
| - | - |
|Type|bit|

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### First_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Middle_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Last_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Title

| Property | Value |
| - | - |
|Type|nvarchar|

### Gender

| Property | Value |
| - | - |
|Type|nvarchar|

### Birth_Date

| Property | Value |
| - | - |
|Type|datetime|

### Nationality

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### National_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Passport_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Passport_Issuing_Date

| Property | Value |
| - | - |
|Type|datetime|

### City

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar|


