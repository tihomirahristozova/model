# Standard Document Attributes

The current article describes standard attributes from the Documents table when a document is created through generation procedure. When the described attributes are not mentioned in a generation procedure, they are filled as follows (* the sub-document is referred as "*sub*"):

- at first, the document route sets the following:

sub.DocumentType = SubDocumentsType;
sub.EnterpriseCompany = SubDocumentsEnterpriseCompany;
sub.EnterpriseCompanyLocation = SubDocumentsEnterpriseCompanyLocation;
sub.ReadOnly = SubDocumentsReadOnly;
sub.ParentDocumentRelationshipType = RelationshipType;
sub.Parent = ParentDocument;

- and then, setting the value in the sub.ParentDocument attribute rises the event of filling in the MasterDocument. This is processed as follows (not the sub-document is current document, so we refer it as "*this*" and the parent document is "*Parent*"):

this.MasterDocument = Parent.MasterDocument;

- and at the end the following attributes are filled in like:

 //set optional attributes if not already set
if (this.EnterpriseCompany == null)
  this.EnterpriseCompany = Parent.EnterpriseCompany;
if (this.EnterpriseCompanyLocation == null)
  this.EnterpriseCompanyLocation = Parent.EnterpriseCompanyLocation;
if (this.CurrencyDirectory == null)
  this.CurrencyDirectory = Parent.CurrencyDirectory;
if (this.DocumentNotes == null)
  this.DocumentNotes = Parent.DocumentNotes;
if (this.FromCompanyDivision == null)
  this.FromCompanyDivision = Parent.FromCompanyDivision;
if (this.ToCompanyDivision == null)
  this.ToCompanyDivision = Parent.ToCompanyDivision;
if (this.FromParty == null)
  this.FromParty = Parent.FromParty;
if (this.ToParty == null)
  this.ToParty = Parent.ToParty;
if (this.ReferenceDate == null)
  this.ReferenceDate = Parent.ReferenceDate;
if (this.ResponsiblePerson == null)
  this.ResponsiblePerson = Parent.ResponsiblePerson;
if (this.ParentDocumentRelationshipType == null)
  this.ParentDocumentRelationshipType = General.ParentDocumentRelationshipType.Subtask;