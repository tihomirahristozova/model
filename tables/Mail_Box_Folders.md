# Table Mail_Box_Folders

Contains the folders inside the mailboxes. Entity: Mail_Box_Folders

# Aggregate Hierarchy

* [Mail_Boxes](Mail_Boxes.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Mail_Box_Folder_Id|`Guid`|`PK`, Readonly||
|Folder_Name|`MultilanguageString`||Multi-language folder name. `Required` `Filter(eq;like)` |
|Server_Folder_ID|`String`||ID of the folder on the mail server in the format of the mail server. `Filter(eq)` |
|Sync_State|`String`||The synchronization state for the folder. The format of the contents is dependant on the server type. For IMAP, this is last message Id, for Exchange - this is SyncState. |
|System_Purpose|`SystemPurpose?`|Allowed: `M`, `I`, `D`, `O`, `S`, `T`, Readonly|When not null means that the folder has special system designation. Designations are: M=Mailbox(root folder), I=Inbox, D=Drafts, O=Outbox, S=Sent, T=Trash. `Filter(eq)` `ReadOnly` |
