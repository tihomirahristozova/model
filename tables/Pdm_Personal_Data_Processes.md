# Table Pdm_Personal_Data_Processes

Represents processes, which process personal data, regulated by GDPR and other applicable laws. Entity: Pdm_Personal_Data_Processes (Introduced in version 18.2)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Personal_Data_Process_Id|`Guid`|`PK`, Readonly||
|Code|`String`||Unique process code. `Required` `Filter(eq;like)` |
|Contains_Sensitive_Data|`Boolean`||True if sensitive personal data is processed (racial, political, criminal, biometric, etc). `Required` `Filter(eq)` |
|Data_Subject_Category|`DataSubjectCategory`|Allowed: `EMP`, `JOB`, `CON`, `CUS`, `SUP`, `PAR`, `OTH`|The category of data subjects (persons), whose data is processed. EMP=Employees; JOB=Job Candidates; CON=Contractors; CUS=Customers; SUP=Suppliers; PAR=Partners; OTH=Other. `Required` |
|Description|`String`||Description of the process. |
|Discontinuation_Date|`DateTime?`||The date on which the process was discontinued. Null if the process is still active. `Filter(eq;ge;le)` |
|Establish_Date|`DateTime`||The data on which the process was established and started functioning. `Required` `Default(Now)` `Filter(eq;ge;le)` |
|Legal_Basis_For_Processing|`LegalBasisForProcessing`|Allowed: `INT`, `CST`, `CTR`, `LEG`, `VIT`, `PUB`|The basis on which the data is processed. INT=Legitimate Interest; CST=Consent; CTR=Contract; LEG=Legal Compliance; VIT=Vital Interests; PUB=Public Interest;. `Required` `Filter(eq)` |
|List_Of_Data_Categories|`String`||Comma-separated list of categories of personal data (both sensitive and non-sensitive) processed by this process. Common sensitive types of data include racial, political views, religion, trade union membership, sex life, criminal records, etc. `Required` `Filter(eq)` |
|List_Of_Data_Recipient_Categories|`String`||Comma-separated list of types of data users. Usual categories include Staff, Public Authority, Contractor, etc. `Filter(eq;like)` |
|List_Of_Processing_Purposes|`String`||Comma-separated list of processing purposes. Common purposes include Invoicing, Newsletter, Notifications, Repeatable Orders, etc. `Filter(eq;like)` |
|List_Of_Technical_Measures|`String`||Comma-separated list of technical measures taken to keep the data privacy. Common measures include Pseudonymisation, Encryption, Data Access Audit, etc. `Filter(eq)` |
|List_Of_Transfers_To_Third_Countries|`String`||Comma-separated list of third countries, to which data is sent. `Filter(eq;like)` |
|List_Of_Used_Software|`String`||Comma-separated list of the names of the software products used to process the data. `Filter(eq;like)` |
|Name|`MultilanguageString`||Name of the process (Multilanguage). `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this PersonalDataProcess. |
|Processing_Role|`ProcessingRole`|Allowed: `C`, `P`|The role of the enterprise company in the process - Controller or Processor. The controller owns the personal data process. The processor operates on behalf of the controller. C=Controller; P=Processor. . `Required` `Default("C")` `Filter(eq)` |
|Retention_Period_Months|`Int32?`||The period in months, for which the data is kept. Null when the period is unknown or N/A. `Filter(eq)` |
|Third_Country_Transfers_Safeguards|`String`||Description of safeguards, taken to protect personal data in case of third country transfers. `Filter(eq;like)` |
