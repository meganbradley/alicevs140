---
title: "CRecordset::RefreshRowset"
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
ms.topic: reference
ms.assetid: a66e0331-1509-4af7-a6ec-206a514cc8bb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::RefreshRowset
Updates the data and the status for a row in the current rowset.  
  
## Syntax  
  
```  
  
      void RefreshRowset(  
   WORD wRow,  
   WORD wLockType = SQL_LOCK_NO_CHANGE   
);  
```  
  
#### Parameters  
 `wRow`  
 The one-based position of a row in the current rowset. This value can range from zero to the size of the rowset.  
  
 `wLockType`  
 A value indicating how to lock the row after it has been refreshed. For details, see Remarks.  
  
## Remarks  
 If you pass a value of zero for `wRow`, then every row in the rowset will be refreshed.  
  
 To use `RefreshRowset`, you must have implemented bulk row fetching by specifying the **CRecordset::useMulitRowFetch** option in the [Open](../vs140/CRecordset--Open.md) member function.  
  
 `RefreshRowset` calls the ODBC API function **SQLSetPos**. The `wLockType` parameter specifies the lock state of the row after **SQLSetPos** has executed. The following table describes the possible values for `wLockTyp`e.  
  
|wLockType|Description|  
|---------------|-----------------|  
|`SQL_LOCK_NO_CHANGE` (the default value)|The driver or data source ensures that the row is in the same locked or unlocked state as it was before `RefreshRowset` was called.|  
|`SQL_LOCK_EXCLUSIVE`|The driver or data source locks the row exclusively. Not all data sources support this type of lock.|  
|`SQL_LOCK_UNLOCK`|The driver or data source unlocks the row. Not all data sources support this type of lock.|  
  
 For more information about **SQLSetPos**, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::SetRowsetCursorPosition](../vs140/CRecordset--SetRowsetCursorPosition.md)   
 [CRecordset::SetRowsetSize](../vs140/CRecordset--SetRowsetSize.md)