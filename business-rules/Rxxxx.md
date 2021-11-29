//---
erp.type: business-rule
erp.entity: logistics-documents
//---

# Rxxxxx LogisticsDocument - Complete Parent Fulfillments

| Name | Value |
| ---- | ----- |
| Code | Rxxxxx |
| Entity | [LogisticsDocument](../reference/common-business-rules/logistics-documents.md) |
| Name | CompleteParentFulfillments |
| Attribute |- |
| Layer | Back-End                                        |
| Events | Completed |
| Priority | Normal |
| Modify | YES |
| Applicable Legislations | ALL // no condition needed |
| Action | If LogiscticsDocument.DocumentType.CompleteParentFulfillments == true, then execute the following steps: <br/><br/> 1. Get the first Logisticcs Document Line. <br/> If LogisticsDocumentLine.ParentDocument == null OR LogisticsDocumentLine.ParentLineNo == null, then skip this line. <br/> Else, continue with step 2. <br/><br/>2. Find all Document Fulfillments, where DocumentFulfillment.DocumentLineId = current.LogisticsDocumentLine.Id <br/><br/>3. For each record found in step 2, create a coresponding Completed record for the parent document line, as follows:<br/><br/>DocumentFulfillment.Document = LogisticsDocumentLine.ParentDocument<br/>DocumentFulfillment.DocumentLineId = FIRST(LogisticsDocument.ParentDocument.ChildLines, where LineNo = LogisticsDocument.ParentLineNo).Id<br/>DocumentFulfillment.LineNo = LogisticsDocument.ParentLineNo<br/>DocumentFulfillment.FulfillmentType = Completed<br/>DocumentFulfillment.IsFinal = false<br/>DocumentFulfillment.LineType = the LineType of the DocumentFulfillment found in step 2<br/>DocumentFulfillment.QuantityBase = the QuantityBase of the DocumentFulfillment found in step 2<br/>DocumentFulfillment.Product = the Product of the DocumentFulfillment found in step 2<br/>DocumentFulfillment.StandardQuantity = the StandardQuantity of the DocumentFulfillment found in step 2<br/>DocumentFulfillment.SerialNumber = the SerialNumber of the DocumentFulfillment found in step 2<br/>DocumentFulfillment.Lot = the Lot of the DocumentFulfillment found in step 2<br/>DocumentFulfillment.ProductVariant = the ProductVariant of the DocumentFulfillment found in step 2 <br/>DocumentFulfillment.CreationUser = the current user <br/> DocumentFulfillment.DestinationEntityName = the entity name of the line of the current document <br/><br/> 4. Repeat step 1, 2 and 3 for all other (if any) Lines of the current document.|
| Description | When document state is changed to Completed, creates Completed document fulfillments for the executed quantities of the parent document lines. <br/> The rule is activated only for documents in whose document type the 'Complete Parent Fulfillments' field is checked. This check-mark and respectively the business rule, are usually used combination with a generation procedure which uses document fulfillments. |
| Message |-|
| Introduced In Version | Introduced: 2022<br>Updated: - |
| Revocable | YES |
