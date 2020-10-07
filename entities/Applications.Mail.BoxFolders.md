# Applications.Mail.BoxFolders

Contains the folders inside the mailboxes. Entity: Mail_Box_Folders

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Mail.BoxFolders.md#Id) | guid |  
| [FolderName](Applications.Mail.BoxFolders.md#FolderName) | [MultilanguageString](../data-types/MultilanguageString.md) | Multi-language folder name. [Required] [Filter(eq;like)] 
| [ServerFolderID](Applications.Mail.BoxFolders.md#ServerFolderID) | string (nullable) | ID of the folder on the mail server in the format of the mail server. [Filter(eq)] 
| [SyncState](Applications.Mail.BoxFolders.md#SyncState) | string (nullable) | The synchronization state for the folder. The format of the contents is dependant on the server type. For IMAP, this is last message Id, for Exchange - this is SyncState. 
| [SystemPurpose](Applications.Mail.BoxFolders.md#SystemPurpose) | [Applications.Mail.BoxFoldersRepository.SystemPurpose](Applications.Mail.BoxFolders.md#SystemPurpose) (nullable) | When not null means that the folder has special system designation. Designations are: M=Mailbox(root folder), I=Inbox, D=Drafts, O=Outbox, S=Sent, T=Trash. [Filter(eq)] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MailBox](Applications.Mail.BoxFolders.md#MailBox) | [Applications.Mail.Boxes](Applications.Mail.Boxes.md) | The [Box](Applications.Mail.Boxes.md) to which this BoxFolder belongs. [Required] [Filter(multi eq)] [ReadOnly] [Owner] |
| [ParentFolder](Applications.Mail.BoxFolders.md#ParentFolder) | [Applications.Mail.BoxFolders](Applications.Mail.BoxFolders.md) (nullable) | The parent folder in the folder hierarchy. Null when the folder is a root folder. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Messages | [Applications.Mail.Messages](Applications.Mail.Messages.md) | List of [Message](Applications.Mail.Messages.md) child objects, based on the [Applications.Mail.Message.MailBoxFolder](Applications.Mail.Messages.md#MailBoxFolder) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FolderName

> Multi-language folder name. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ServerFolderID

> ID of the folder on the mail server in the format of the mail server. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### SyncState

> The synchronization state for the folder. The format of the contents is dependant on the server type. For IMAP, this is last message Id, for Exchange - this is SyncState.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SystemPurpose

> When not null means that the folder has special system designation. Designations are: M=Mailbox(root folder), I=Inbox, D=Drafts, O=Outbox, S=Sent, T=Trash. [Filter(eq)] [ReadOnly]

_Type_: **[Applications.Mail.BoxFoldersRepository.SystemPurpose](Applications.Mail.BoxFolders.md#SystemPurpose) (nullable)**  
Allowed values for the [SystemPurpose](Applications.Mail.BoxFolders.md#SystemPurpose) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Mailbox | Mailbox value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Mailbox' |
| Inbox | Inbox value. Stored as 'I'. <br /> _Database Value:_ 'I' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Inbox' |
| Drafts | Drafts value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Drafts' |
| Outbox | Outbox value. Stored as 'O'. <br /> _Database Value:_ 'O' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Outbox' |
| Sent | Sent value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Sent' |
| Trash | Trash value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Trash' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  


## Reference Details

### MailBox

> The [Box](Applications.Mail.Boxes.md) to which this BoxFolder belongs. [Required] [Filter(multi eq)] [ReadOnly] [Owner]

_Type_: **[Applications.Mail.Boxes](Applications.Mail.Boxes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ParentFolder

> The parent folder in the folder hierarchy. Null when the folder is a root folder. [Filter(multi eq)]

_Type_: **[Applications.Mail.BoxFolders](Applications.Mail.BoxFolders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Mail.BoxFolders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Mail.BoxFolders erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Mail.BoxFolders erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Mail_BoxFolders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Mail_BoxFolders?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Mail_Box_Folders?$top=10>

