---
uid: Applications.PersonalData.PersonalDataProcesses
---
# Applications.PersonalData.PersonalDataProcesses

Represents processes, which process personal data, regulated by GDPR and other applicable laws. Entity: Pdm_Personal_Data_Processes (Introduced in version 18.2.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.PersonalData.PersonalDataProcesses.md#Id) | guid |  
| [Code](Applications.PersonalData.PersonalDataProcesses.md#Code) | string | Unique process code. [Required] [Filter(eq;like)] 
| [ContainsSensitiveData](Applications.PersonalData.PersonalDataProcesses.md#ContainsSensitiveData) | boolean | True if sensitive personal data is processed (racial, political, criminal, biometric, etc). [Required] [Filter(eq)] 
| [DataSubjectCategory](Applications.PersonalData.PersonalDataProcesses.md#DataSubjectCategory) | [Applications.PersonalData.PersonalDataProcessesRepository.DataSubjectCategory](Applications.PersonalData.PersonalDataProcesses.md#DataSubjectCategory) | The category of data subjects (persons), whose data is processed. EMP=Employees; JOB=Job Candidates; CON=Contractors; CUS=Customers; SUP=Suppliers; PAR=Partners; OTH=Other. [Required] 
| [Description](Applications.PersonalData.PersonalDataProcesses.md#Description) | string (nullable) | Description of the process. 
| [DiscontinuationDate](Applications.PersonalData.PersonalDataProcesses.md#DiscontinuationDate) | date (nullable) | The date on which the process was discontinued. Null if the process is still active. [Filter(eq;ge;le)] 
| [EstablishDate](Applications.PersonalData.PersonalDataProcesses.md#EstablishDate) | date | The data on which the process was established and started functioning. [Required] [Default(Now)] [Filter(eq;ge;le)] 
| [LegalBasisForProcessing](Applications.PersonalData.PersonalDataProcesses.md#LegalBasisForProcessing) | [Applications.PersonalData.PersonalDataProcessesRepository.LegalBasisForProcessing](Applications.PersonalData.PersonalDataProcesses.md#LegalBasisForProcessing) | The basis on which the data is processed. INT=Legitimate Interest; CST=Consent; CTR=Contract; LEG=Legal Compliance; VIT=Vital Interests; PUB=Public Interest;. [Required] [Filter(eq)] 
| [ListOfDataCategories](Applications.PersonalData.PersonalDataProcesses.md#ListOfDataCategories) | string | Comma-separated list of categories of personal data (both sensitive and non-sensitive) processed by this process. Common sensitive types of data include racial, political views, religion, trade union membership, sex life, criminal records, etc. [Required] [Filter(eq)] 
| [ListOfDataRecipientCategories](Applications.PersonalData.PersonalDataProcesses.md#ListOfDataRecipientCategories) | string (nullable) | Comma-separated list of types of data users. Usual categories include Staff, Public Authority, Contractor, etc. [Filter(eq;like)] 
| [ListOfProcessingPurposes](Applications.PersonalData.PersonalDataProcesses.md#ListOfProcessingPurposes) | string (nullable) | Comma-separated list of processing purposes. Common purposes include Invoicing, Newsletter, Notifications, Repeatable Orders, etc. [Filter(eq;like)] 
| [ListOfTechnicalMeasures](Applications.PersonalData.PersonalDataProcesses.md#ListOfTechnicalMeasures) | string (nullable) | Comma-separated list of technical measures taken to keep the data privacy. Common measures include Pseudonymisation, Encryption, Data Access Audit, etc. [Filter(eq)] 
| [ListOfTransfersToThirdCountries](Applications.PersonalData.PersonalDataProcesses.md#ListOfTransfersToThirdCountries) | string (nullable) | Comma-separated list of third countries, to which data is sent. [Filter(eq;like)] 
| [ListOfUsedSoftware](Applications.PersonalData.PersonalDataProcesses.md#ListOfUsedSoftware) | string (nullable) | Comma-separated list of the names of the software products used to process the data. [Filter(eq;like)] 
| [Name](Applications.PersonalData.PersonalDataProcesses.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Name of the process (Multilanguage). [Required] [Filter(eq;like)] 
| [Notes](Applications.PersonalData.PersonalDataProcesses.md#Notes) | string (nullable) | Notes for this PersonalDataProcess. 
| [ProcessingRole](Applications.PersonalData.PersonalDataProcesses.md#ProcessingRole) | [Applications.PersonalData.PersonalDataProcessesRepository.ProcessingRole](Applications.PersonalData.PersonalDataProcesses.md#ProcessingRole) | The role of the enterprise company in the process - Controller or Processor. The controller owns the personal data process. The processor operates on behalf of the controller. C=Controller; P=Processor. . [Required] [Default("C")] [Filter(eq)] 
| [RetentionPeriodMonths](Applications.PersonalData.PersonalDataProcesses.md#RetentionPeriodMonths) | int32 (nullable) | The period in months, for which the data is kept. Null when the period is unknown or N/A. [Filter(eq)] 
| [ThirdCountryTransfersSafeguards](Applications.PersonalData.PersonalDataProcesses.md#ThirdCountryTransfersSafeguards) | string (nullable) | Description of safeguards, taken to protect personal data in case of third country transfers. [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Applications.PersonalData.PersonalDataProcesses.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company, which owns the process. [Required] [Filter(multi eq)] |
| [ProcessOwnerPerson](Applications.PersonalData.PersonalDataProcesses.md#ProcessOwnerPerson) | [General.Contacts.Persons](General.Contacts.Persons.md) | The owner and responsible person for the process. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| JointControllers | [Applications.PersonalData.JointControllers](Applications.PersonalData.JointControllers.md) | List of [JointController](Applications.PersonalData.JointControllers.md) child objects, based on the [Applications.PersonalData.JointController.PersonalDataProcess](Applications.PersonalData.JointControllers.md#PersonalDataProcess) back reference 
| Recipients | [Applications.PersonalData.PersonalDataProcessRecipients](Applications.PersonalData.PersonalDataProcessRecipients.md) | List of [PersonalDataProcessRecipient](Applications.PersonalData.PersonalDataProcessRecipients.md) child objects, based on the [Applications.PersonalData.PersonalDataProcessRecipient.PersonalDataProcess](Applications.PersonalData.PersonalDataProcessRecipients.md#PersonalDataProcess) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> Unique process code. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ContainsSensitiveData

> True if sensitive personal data is processed (racial, political, criminal, biometric, etc). [Required] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### DataSubjectCategory

> The category of data subjects (persons), whose data is processed. EMP=Employees; JOB=Job Candidates; CON=Contractors; CUS=Customers; SUP=Suppliers; PAR=Partners; OTH=Other. [Required]

_Type_: **[Applications.PersonalData.PersonalDataProcessesRepository.DataSubjectCategory](Applications.PersonalData.PersonalDataProcesses.md#DataSubjectCategory)**  
Allowed values for the [DataSubjectCategory](Applications.PersonalData.PersonalDataProcesses.md#DataSubjectCategory) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Employees | Employees value. Stored as 'EMP'. <br /> _Database Value:_ 'EMP' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Employees' |
| JobCandidates | JobCandidates value. Stored as 'JOB'. <br /> _Database Value:_ 'JOB' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'JobCandidates' |
| Contractors | Contractors value. Stored as 'CON'. <br /> _Database Value:_ 'CON' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Contractors' |
| Customers | Customers value. Stored as 'CUS'. <br /> _Database Value:_ 'CUS' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Customers' |
| Suppliers | Suppliers value. Stored as 'SUP'. <br /> _Database Value:_ 'SUP' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Suppliers' |
| Partners | Partners value. Stored as 'PAR'. <br /> _Database Value:_ 'PAR' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Partners' |
| Other | Other value. Stored as 'OTH'. <br /> _Database Value:_ 'OTH' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'Other' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Description

> Description of the process.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DiscontinuationDate

> The date on which the process was discontinued. Null if the process is still active. [Filter(eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### EstablishDate

> The data on which the process was established and started functioning. [Required] [Default(Now)] [Filter(eq;ge;le)]

_Type_: **date**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### LegalBasisForProcessing

> The basis on which the data is processed. INT=Legitimate Interest; CST=Consent; CTR=Contract; LEG=Legal Compliance; VIT=Vital Interests; PUB=Public Interest;. [Required] [Filter(eq)]

_Type_: **[Applications.PersonalData.PersonalDataProcessesRepository.LegalBasisForProcessing](Applications.PersonalData.PersonalDataProcesses.md#LegalBasisForProcessing)**  
Allowed values for the [LegalBasisForProcessing](Applications.PersonalData.PersonalDataProcesses.md#LegalBasisForProcessing) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| LegitimateInterest | LegitimateInterest value. Stored as 'INT'. <br /> _Database Value:_ 'INT' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'LegitimateInterest' |
| Consent | Consent value. Stored as 'CST'. <br /> _Database Value:_ 'CST' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Consent' |
| Contract | Contract value. Stored as 'CTR'. <br /> _Database Value:_ 'CTR' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Contract' |
| LegalCompliance | LegalCompliance value. Stored as 'LEG'. <br /> _Database Value:_ 'LEG' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'LegalCompliance' |
| VitalInterest | VitalInterest value. Stored as 'VIT'. <br /> _Database Value:_ 'VIT' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'VitalInterest' |
| PublicInterest | PublicInterest value. Stored as 'PUB'. <br /> _Database Value:_ 'PUB' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'PublicInterest' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ListOfDataCategories

> Comma-separated list of categories of personal data (both sensitive and non-sensitive) processed by this process. Common sensitive types of data include racial, political views, religion, trade union membership, sex life, criminal records, etc. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ListOfDataRecipientCategories

> Comma-separated list of types of data users. Usual categories include Staff, Public Authority, Contractor, etc. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ListOfProcessingPurposes

> Comma-separated list of processing purposes. Common purposes include Invoicing, Newsletter, Notifications, Repeatable Orders, etc. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ListOfTechnicalMeasures

> Comma-separated list of technical measures taken to keep the data privacy. Common measures include Pseudonymisation, Encryption, Data Access Audit, etc. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ListOfTransfersToThirdCountries

> Comma-separated list of third countries, to which data is sent. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ListOfUsedSoftware

> Comma-separated list of the names of the software products used to process the data. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Name

> Name of the process (Multilanguage). [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this PersonalDataProcess.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProcessingRole

> The role of the enterprise company in the process - Controller or Processor. The controller owns the personal data process. The processor operates on behalf of the controller. C=Controller; P=Processor. . [Required] [Default("C")] [Filter(eq)]

_Type_: **[Applications.PersonalData.PersonalDataProcessesRepository.ProcessingRole](Applications.PersonalData.PersonalDataProcesses.md#ProcessingRole)**  
Allowed values for the [ProcessingRole](Applications.PersonalData.PersonalDataProcesses.md#ProcessingRole) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Controller | Controller value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Controller' |
| Processor | Processor value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Processor' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Controller**  

### RetentionPeriodMonths

> The period in months, for which the data is kept. Null when the period is unknown or N/A. [Filter(eq)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ThirdCountryTransfersSafeguards

> Description of safeguards, taken to protect personal data in case of third country transfers. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company, which owns the process. [Required] [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProcessOwnerPerson

> The owner and responsible person for the process. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.PersonalData.PersonalDataProcesses erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.PersonalData.PersonalDataProcesses erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.PersonalData.PersonalDataProcesses erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_PersonalData_PersonalDataProcesses?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_PersonalData_PersonalDataProcesses?$top=10>

