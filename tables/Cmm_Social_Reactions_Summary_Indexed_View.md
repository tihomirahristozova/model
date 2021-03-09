# View Cmm_Social_Reactions_Summary_Indexed_View

Summary with the social reactions per comment and dataobject. Entity: Cmm_Social_Reactions_Summary_Indexed_View

## Summary

| Name | Type | Description |
| - | - | --- |
|[Data_Object_Id](#data_object_id)|`uniqueidentifier` ||
|[Social_Comment_Id](#social_comment_id)|`uniqueidentifier` ||
|[Reaction_Type](#reaction_type)|`nvarchar(3)` Allowed: `LIK`, `LOV`, `HAH`, `WOW`, `SAD`, `ANG`|The type of the reaction. LIK = Like; LOV = Love; HAH = Haha; WOW = Wow; SAD = Sad; ANG = Angry.|
|[Cnt](#cnt)|`bigint` ||

## Columns

### Data_Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Social_Comment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reaction_Type

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Cnt

| Property | Value |
| - | - |
|Type|bigint|


