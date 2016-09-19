---
title: "Recordset: Adding Records in Bulk (ODBC)"
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
ms.assetid: 4685f656-14b9-4f10-a1c5-147b2b89a0b4
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Recordset: Adding Records in Bulk (ODBC)
This topic applies to the MFC ODBC classes.  
  
 The MFC [CRecordset](../vs140/CRecordset-Class.md) class has a new optimization that improves efficiency when you are adding new records in bulk to a table.  
  
> [!NOTE]
>  This topic applies to objects derived from `CRecordset` in which bulk row fetching has not been implemented. If you are using bulk row fetching, see [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
 A new option for the **dwOptions** parameter to the [CRecordset::Open](../vs140/CRecordset--Open.md) member function, **optimizeBulkAdd**, improves performance when you are adding multiple records consecutively without calling **Requery** or **Close**. Only those fields that are dirty before the first **Update** call are marked as dirty for subsequent `AddNew`/**Update** calls.  
  
 If you are using the database classes to take advantage of the **::SQLSetPos** ODBC API function for adding, editing, and deleting records, this optimization is unnecessary.  
  
 If the ODBC Cursor Library is loaded or the ODBC driver does not support adding, editing, and deleting through **::SQLSetPos**, this optimization should improve bulk add performance. To turn on this optimization, set the **dwOptions** parameter in the **Open** call for your recordset to the following:  
  
```  
appendOnly | optimizeBulkAdd  
```  
  
## See Also  
 [Recordset (ODBC)](../vs140/Recordset--ODBC-.md)   
 [Recordset: Adding, Updating, and Deleting Records (ODBC)](../vs140/Recordset--Adding--Updating--and-Deleting-Records--ODBC-.md)   
 [Recordset: Locking Records (ODBC)](../vs140/Recordset--Locking-Records--ODBC-.md)