# Table Pdm_Personal_Data_Processes

Represents processes, which process personal data, regulated by GDPR and other applicable laws. Entity: Pdm_Personal_Data_Processes (Introduced in version 18.2)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Personal_Data_Process_Id](#personal_data_process_id)|`uniqueidentifier` `PK`|Personal Data Management Process|
|[Code](#code)|`nvarchar(16)` |Unique process code.|
|[Name](#name)|`nvarchar(254)` `ML`|Name of the process (Multilanguage).|
|[Description](#description)|`nvarchar(2147483647)` |Description of the process.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company, which owns the process.|
|[Processing_Role](#processing_role)|`nvarchar(1)` Allowed: `C`, `P`|The role of the enterprise company in the process - Controller or Processor. The controller owns the personal data process. The processor operates on behalf of the controller. C=Controller; P=Processor. |
|[Retention_Period_Months](#retention_period_months)|`int` |The period in months, for which the data is kept. Null when the period is unknown or N/A.|
|[List_Of_Used_Software](#list_of_used_software)|`nvarchar(254)` |Comma-separated list of the names of the software products used to process the data.|
|[Process_Owner_Person_Id](#process_owner_person_id)|`uniqueidentifier` |The owner and responsible person for the process.|
|[List_Of_Technical_Measures](#list_of_technical_measures)|`nvarchar(254)` |Comma-separated list of technical measures taken to keep the data privacy. Common measures include Pseudonymisation, Encryption, Data Access Audit, etc.|
|[Data_Subject_Category](#data_subject_category)|`nvarchar(3)` Allowed: `EMP`, `JOB`, `CON`, `CUS`, `SUP`, `PAR`, `OTH`|The category of data subjects (persons), whose data is processed. EMP=Employees; JOB=Job Candidates; CON=Contractors; CUS=Customers; SUP=Suppliers; PAR=Partners; OTH=Other.|
|[Contains_Sensitive_Data](#contains_sensitive_data)|`bit` |True if sensitive personal data is processed (racial, political, criminal, biometric, etc).|
|[List_Of_Data_Categories](#list_of_data_categories)|`nvarchar(254)` |Comma-separated list of categories of personal data (both sensitive and non-sensitive) processed by this process. Common sensitive types of data include racial, political views, religion, trade union membership, sex life, criminal records, etc.|
|[Legal_Basis_For_Processing](#legal_basis_for_processing)|`nvarchar(3)` Allowed: `INT`, `CST`, `CTR`, `LEG`, `VIT`, `PUB`|The basis on which the data is processed. INT=Legitimate Interest; CST=Consent; CTR=Contract; LEG=Legal Compliance; VIT=Vital Interests; PUB=Public Interest;|
|[List_Of_Data_Recipient_Categories](#list_of_data_recipient_categories)|`nvarchar(254)` |Comma-separated list of types of data users. Usual categories include Staff, Public Authority, Contractor, etc.|
|[List_Of_Processing_Purposes](#list_of_processing_purposes)|`nvarchar(254)` |Comma-separated list of processing purposes. Common purposes include Invoicing, Newsletter, Notifications, Repeatable Orders, etc.|
|[List_Of_Transfers_To_Third_Countries](#list_of_transfers_to_third_countries)|`nvarchar(254)` |Comma-separated list of third countries, to which data is sent.|
|[Third_Country_Transfers_Safeguards](#third_country_transfers_safeguards)|`nvarchar(254)` |Description of safeguards, taken to protect personal data in case of third country transfers.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Establish_Date](#establish_date)|`date` |The data on which the process was established and started functioning.|
|[Discontinuation_Date](#discontinuation_date)|`date` |The date on which the process was discontinued. Null if the process is still active.|

## Columns

### Personal_Data_Process_Id


Personal_Data_Process_Id


Personal Data Management Process


Personal Data Management Process

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Personal_Data_Process_Id](Pdm_Personal_Data_Processes.md#personal_data_process_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Code


Code


Unique process code.


Unique process code.

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Code](Pdm_Personal_Data_Processes.md#code)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|16|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Name


Name


Name of the process (Multilanguage).


Name of the process (Multilanguage).

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Name](Pdm_Personal_Data_Processes.md#name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Description


Description


Description of the process.


Description of the process.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Description](Pdm_Personal_Data_Processes.md#description)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Enterprise_Company_Id


Enterprise_Company_Id


The enterprise company, which owns the process.


The enterprise company, which owns the process.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Enterprise_Company_Id](Pdm_Personal_Data_Processes.md#enterprise_company_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Processing_Role


Processing_Role


The role of the enterprise company in the process - Controller or Processor. The controller owns the personal data process. The processor operates on behalf of the controller. C=Controller; P=Processor. 


The role of the enterprise company in the process - Controller or Processor. The controller owns the personal data process. The processor operates on behalf of the controller. C=Controller; P=Processor. 

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`C`, `P`|
|Default Value|C|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Processing_Role](Pdm_Personal_Data_Processes.md#processing_role)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Retention_Period_Months


Retention_Period_Months


The period in months, for which the data is kept. Null when the period is unknown or N/A.


The period in months, for which the data is kept. Null when the period is unknown or N/A.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Retention_Period_Months](Pdm_Personal_Data_Processes.md#retention_period_months)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### List_Of_Used_Software


List_Of_Used_Software


Comma-separated list of the names of the software products used to process the data.


Comma-separated list of the names of the software products used to process the data.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[List_Of_Used_Software](Pdm_Personal_Data_Processes.md#list_of_used_software)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Process_Owner_Person_Id


Process_Owner_Person_Id


The owner and responsible person for the process.


The owner and responsible person for the process.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Persons](Cm_Persons.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Process_Owner_Person_Id](Pdm_Personal_Data_Processes.md#process_owner_person_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### List_Of_Technical_Measures


List_Of_Technical_Measures


Comma-separated list of technical measures taken to keep the data privacy. Common measures include Pseudonymisation, Encryption, Data Access Audit, etc.


Comma-separated list of technical measures taken to keep the data privacy. Common measures include Pseudonymisation, Encryption, Data Access Audit, etc.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[List_Of_Technical_Measures](Pdm_Personal_Data_Processes.md#list_of_technical_measures)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Data_Subject_Category


Data_Subject_Category


The category of data subjects (persons), whose data is processed. EMP=Employees; JOB=Job Candidates; CON=Contractors; CUS=Customers; SUP=Suppliers; PAR=Partners; OTH=Other.


The category of data subjects (persons), whose data is processed. EMP=Employees; JOB=Job Candidates; CON=Contractors; CUS=Customers; SUP=Suppliers; PAR=Partners; OTH=Other.

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`EMP`, `JOB`, `CON`, `CUS`, `SUP`, `PAR`, `OTH`|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Data_Subject_Category](Pdm_Personal_Data_Processes.md#data_subject_category)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|3|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Contains_Sensitive_Data


Contains_Sensitive_Data


True if sensitive personal data is processed (racial, political, criminal, biometric, etc).


True if sensitive personal data is processed (racial, political, criminal, biometric, etc).

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Contains_Sensitive_Data](Pdm_Personal_Data_Processes.md#contains_sensitive_data)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### List_Of_Data_Categories


List_Of_Data_Categories


Comma-separated list of categories of personal data (both sensitive and non-sensitive) processed by this process. Common sensitive types of data include racial, political views, religion, trade union membership, sex life, criminal records, etc.


Comma-separated list of categories of personal data (both sensitive and non-sensitive) processed by this process. Common sensitive types of data include racial, political views, religion, trade union membership, sex life, criminal records, etc.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[List_Of_Data_Categories](Pdm_Personal_Data_Processes.md#list_of_data_categories)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Legal_Basis_For_Processing


Legal_Basis_For_Processing


The basis on which the data is processed. INT=Legitimate Interest; CST=Consent; CTR=Contract; LEG=Legal Compliance; VIT=Vital Interests; PUB=Public Interest;


The basis on which the data is processed. INT=Legitimate Interest; CST=Consent; CTR=Contract; LEG=Legal Compliance; VIT=Vital Interests; PUB=Public Interest;

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`INT`, `CST`, `CTR`, `LEG`, `VIT`, `PUB`|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Legal_Basis_For_Processing](Pdm_Personal_Data_Processes.md#legal_basis_for_processing)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|3|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### List_Of_Data_Recipient_Categories


List_Of_Data_Recipient_Categories


Comma-separated list of types of data users. Usual categories include Staff, Public Authority, Contractor, etc.


Comma-separated list of types of data users. Usual categories include Staff, Public Authority, Contractor, etc.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[List_Of_Data_Recipient_Categories](Pdm_Personal_Data_Processes.md#list_of_data_recipient_categories)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### List_Of_Processing_Purposes


List_Of_Processing_Purposes


Comma-separated list of processing purposes. Common purposes include Invoicing, Newsletter, Notifications, Repeatable Orders, etc.


Comma-separated list of processing purposes. Common purposes include Invoicing, Newsletter, Notifications, Repeatable Orders, etc.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[List_Of_Processing_Purposes](Pdm_Personal_Data_Processes.md#list_of_processing_purposes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### List_Of_Transfers_To_Third_Countries


List_Of_Transfers_To_Third_Countries


Comma-separated list of third countries, to which data is sent.


Comma-separated list of third countries, to which data is sent.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[List_Of_Transfers_To_Third_Countries](Pdm_Personal_Data_Processes.md#list_of_transfers_to_third_countries)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Third_Country_Transfers_Safeguards


Third_Country_Transfers_Safeguards


Description of safeguards, taken to protect personal data in case of third country transfers.


Description of safeguards, taken to protect personal data in case of third country transfers.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Third_Country_Transfers_Safeguards](Pdm_Personal_Data_Processes.md#third_country_transfers_safeguards)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Notes](Pdm_Personal_Data_Processes.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Row_Version](Pdm_Personal_Data_Processes.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Establish_Date


Establish_Date


The data on which the process was established and started functioning.


The data on which the process was established and started functioning.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTime|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Establish_Date](Pdm_Personal_Data_Processes.md#establish_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|GreaterThanOrLessThan|None|no|no|

### Discontinuation_Date


Discontinuation_Date


The date on which the process was discontinued. Null if the process is still active.


The date on which the process was discontinued. Null if the process is still active.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md).[Discontinuation_Date](Pdm_Personal_Data_Processes.md#discontinuation_date)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|GreaterThanOrLessThan|None|no|no|


