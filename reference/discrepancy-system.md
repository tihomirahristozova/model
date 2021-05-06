# Discrepancy System

The purpose of the *Discrepancy System* is: when sub-documents are generated from a parent document, the values in the sub-documents to be calculated so the parent document is properly fulfilled, i.e. not to be partially or over-executed (except if the user wants it).

The *Discrepancy System* works as follows:

1. First, the unfulfilled part of the parent document is defined. This is executed by loading (parts of) already created sub-documents;
2. Then the new sub-documents are created and saved in the database only for the unfulfilled parts (including over-execution) of the parent document.

The current article describes step 1 of the *Discrepancy System*. Step 2 is described individually for in each document generation procedure.

Defining the fulfilled part of a parent document consists of two main activities - calculating the fulfilled part and defining the discrepancy between the data in the current document and the summed up data from the sub-documents.

## Loading The Fulfilled Part

Usually, in one generation procedure of sub-documents from a parent document, there is one central part (essential for the procedure) of sub-documents, which is enough for defining the fulfillment of the parent document. 
In most cases these are the sub-documents rows. 
Usually, they contain the necessary data - quantities and amounts. Of course, there is an exception of this rule.
For example, when generating Payment Orders the essentials are the headers of the Payment Orders as they contain the amounts to pay (Payment Orders does not have rows).

Data is loaded only from sub-documents which are **created from the current parent document** (i.e. in them the field "Parent Document" is filled with exactly this parent document) and which are **not-voided** and **have document state at least "Planned".**

It is possible the loaded document data to contain data not related to the fulfilled part of the parent document. 
For example, if in the sub-document the user manually add new row and fill in that the current row is related to a non-existing parent row.
Such data in the sub-documents is a problem as later in the parent document a row with that number may be added and suddenly the data in the sub-document will become its fulfillment, which may be wrong (it is possible that there is no meaningful connection between the data in the sub-document and the newly added row in the parent document).
This is why, if in the sub-documents such data is found (which corresponds with non-existing parts of the parent document), then the current activities of the system should end by error message.

### Example 1:

When Invoices are generated from Invoice Orders, the rows of the already created Invoices from the sub-documents are loaded. If the Invoice Order have the following rows:

- row #1: LineNo = **10**; Quantity = **10 PCS**; Line Amount = **120 EUR**;
- row #2: LineNo = **20**; Quantity = **76 PCS**; Line Amount = **63 EUR**;

and there are no Invoices created by now, then the loaded data will be an empty set of rows:

**[Invoices fulfillment] = { }**

In this case the Invoice Order is completely unfulfilled.

### Example 2:

In the current case Payment Orders are created from Sales Orders. There are two Sales Orders with the following payment plans:

- Sales Order #1:
  - Installment **1** - Amount **70 EUR**;
  - Installment **2** - Amount **25 EUR**;
  - Installment **3** - Amount **40 EUR**;

- Sales Order #2:

  - Installment **1** - Amount **100 EUR**;

Sub-documents of Payment Orders are already created as follows:

- Payment Order #**1**: Parent Document = **Sales Order #1**, Installment = **#1**, Total Amount = **70 EUR**;
- Payment Order #**2**: Parent Document = **Sales Order #1**, Installment = **#2**, Total Amount = **15 EUR**;
- Payment Order #**3**: Parent Document = **Sales Order #2**, Installment = **#1**, Total Amount = **33 EUR**;

Then the fulfilled part from Sales Order #1 is:

**[Sales Order fulfillment]** = { Payment Order #1, Payment Order #2 }

The last Payment Order is not part of the set above as it is a sub-document of other Sales Order.
It is clear that the Sales Order is partially fulfilled by the Payment Orders. Some of the installments are completely fulfilled, others are partially fulfilled, and there are installments that are not fulfilled at all.

### Example 3:

In the current example there are two stores - Store 1 and Store 2. Then, there is the following **Sales Order #1**:

- Store - Store 1;

    - row #1 - Quantity = **10 PCS**;
    - row #2 - Quantity = **8 PCS**;

Two Store Orders are created (note that the second Store Order contains a row that refers to a non-existing Sales Order row):

- Store Order #1:
  - Parent Document - **Sales Order #1**;
  - Store -  Store 1;

    - row #1 - ParentLineNo = 10; Quantity - **10 PCS**;
    - row #2 - ParentLineNo = **20**; Quantity - **2 PCS**;

- Store Order #2:

  - Parent Document - **Sales Order #1**;

  - Store - Store 2;

    - row #1 - ParentLineNo = **30**; Quantity - **3 PCS**;

In this case the loaded data that will be executed is:

**[Store Order fulfillment]** = { Store Order #1 row #1, Store Order #1 row#2, Store Order #2 row #1 }

This data shows that the two Store Order rows are fulfilled but the second Store Order contains a row referring to Store Order row #30. 
As such row does not exist in the Store Order - the current action stops with error message.

## Defining the unfulfilled part of the document

The procedure of defining the unfulfilled part of the document happens after loading the fulfillment of the parent document and this fulfillment is written off from the data (usually this is executed on scalar-value fields such as Quantity and Amounts) from the document.

This is not executed for all scalar-valued fields from the parent document.
For example, when Invoices are created from Invoice Orders, this is proceeded for both scalar-value fields in the orders rows - both for Quantity and for Line Amount. But when Store Orders are created from the Sales Orders, the calculation is applied only for the quantities in the rows of the Sales Order.
The reason is that the amounts from the Sales Order rows does not participate in the Store Orders creation.

If we expand the examples from above:

### Example 1 (part2):

For each row from the Invoice Order we have to define two values - the quantity left to be invoiced and the amount left to be invoiced.
As **[Invoices fulfillment]** is an empty set then these values are the whole quantities and amounts from the rows:

- row #1 - Remaining Quantity = **10 PCS**, Remaining Amount = **120 EUR**;
- row #2 - Remaining Quantity = **7 PCS**, Remaining Amount = **63 EUR**;

There is no over-execution. So in this case the created Invoicehas the same quantities and amounts as in the Invoice Order.

### Example 2 (part2):

In this case the unfulfilled part from the first Sales Order is:

- Installment **1** - Remaining Amount = **70 EUR - 70 EUR = 0 EUR**;
- Installment **2** - Remaining Amount = **25 EUR - 15 EUR = 10 EUR**;
- Installment **3** - Remaining Amount = **40 EUR - 0 EUR = 40 EUR**;

There are no over-executions in this case either as no installment has Payment Orders with total amount larger then the amount in the installment.
So in this case the Payment Orders that have to be created contain only for the remaining amounts - **10 EUR** and **40 EUR** - for the last two installments.
