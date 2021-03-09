# Query Gen_Party_Pictures_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Party_Picture_Id](#party_picture_id)|`uniqueidentifier` `PK`||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Picture_No](#picture_no)|`int` |Unique picture number within the party. Also used for sorting|
|[Comments](#comments)|`nvarchar` |Notes for this party picture.|
|[Picture](#picture)|`varbinary` |The actual party picture data. Can be NULL if we insert only some comments.|
|[Is_Default](#is_default)|`bit` |1=This is the default picture for the party; 0=otherwise|
|[Is_Logo](#is_logo)|`bit` ||
|[Is_Active](#is_active)|`bit` ||

## Columns

### Party_Picture_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Picture_No

| Property | Value |
| - | - |
|Type|int|

### Comments

| Property | Value |
| - | - |
|Type|nvarchar|

### Picture

| Property | Value |
| - | - |
|Type|varbinary|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Is_Logo

| Property | Value |
| - | - |
|Type|bit|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|


