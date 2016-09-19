---
title: "Transaction (ODBC)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a2ec0995-2029-45f2-8092-6efd6f2a77f4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Transaction (ODBC)
This topic applies to the MFC ODBC classes.  
  
 A transaction is a way to group, or batch, a series of updates to a [data source](../vs140/Data-Source--ODBC-.md) so that all are committed at once or none are committed if you roll back the transaction. If you do not use a transaction, changes to the data source are committed automatically rather than being committed on demand.  
  
> [!NOTE]
>  Not all ODBC database drivers support transactions. Call the `CanTransact` member function of your [CDatabase](../vs140/CDatabase-Class.md) or [CRecordset](../vs140/CRecordset-Class.md) object to determine whether your driver supports transactions for a given database. Note that `CanTransact` does not tell you whether the data source provides full transaction support. You must also call `CDatabase::GetCursorCommitBehavior` and `CDatabase::GetCursorRollbackBehavior` after **CommitTrans** and **Rollback** to check the effect of the transaction on the open `CRecordset` object.  
  
 Calls to the `AddNew` and **Edit** member functions of a `CRecordset` object affect the data source immediately when you call **Update**. **Delete** calls also take effect immediately. In contrast, you can use a transaction consisting of multiple calls to `AddNew`, **Edit**, **Update**, and **Delete**, which are performed but not committed until you call **CommitTrans** explicitly. By establishing a transaction, you can execute a series of such calls while retaining the ability to roll them back. If a critical resource is unavailable or some other condition prevents the entire transaction from being completed, you can roll back the transaction instead of committing it. In that case, none of the changes belonging to the transaction affect the data source.  
  
> [!NOTE]
>  Currently, class `CRecordset` does not support updates to the data source if you have implemented bulk row fetching. This means you cannot make calls to `AddNew`, **Edit**, **Delete**, or **Update**. However, you can write you own functions to perform updates and then call those functions within a given transaction. For more information about bulk row fetching, see [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
> [!NOTE]
>  Besides affecting your recordset, transactions affect SQL statements that you execute directly as long as you use the ODBC **HDBC** associated with your `CDatabase` object or an ODBC **HSTMT** based on that **HDBC**.  
  
 Transactions are particularly useful when you have multiple records that must be updated simultaneously. In this case, you want to avoid a half-completed transaction, such as might happen if an exception was thrown before the last update was made. Grouping such updates into a transaction allows a recovery (rollback) from the changes and returns the records to the pretransaction state. For example, if a bank transfers money from account A to account B, both the withdrawal from A and the deposit to B must succeed to process the funds correctly or the whole transaction must fail.  
  
 In the database classes, you perform transactions through `CDatabase` objects. A `CDatabase` object represents a connection to a data source, and one or more recordsets associated with that `CDatabase` object operate on tables of the database through recordset member functions.  
  
> [!NOTE]
>  Only one level of transactions is supported. You cannot nest transactions nor can a transaction span multiple database objects.  
  
 The following topics provide more information about how transactions are performed:  
  
-   [Transaction: Performing a Transaction in a Recordset (ODBC)](../vs140/Transaction--Performing-a-Transaction-in-a-Recordset--ODBC-.md)  
  
-   [Transaction: How Transactions Affect Updates (ODBC)](../vs140/Transaction--How-Transactions-Affect-Updates--ODBC-.md)  
  
## See Also  
 [Open Database Connectivity (ODBC)](../vs140/Open-Database-Connectivity--ODBC-.md)