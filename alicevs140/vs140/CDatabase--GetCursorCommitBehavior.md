---
title: "CDatabase::GetCursorCommitBehavior"
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
ms.assetid: 84e516c5-69a9-4d00-8eca-70fdf02fdb0d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDatabase::GetCursorCommitBehavior
Call this member function to determine how a [CommitTrans](../vs140/CDatabase--CommitTrans.md) operation affects cursors on open recordset objects.  
  
## Syntax  
  
```  
  
int GetCursorCommitBehavior( ) const;  
  
```  
  
## Return Value  
 A value indicating the effect of transactions on open recordset objects. For details, see Remarks.  
  
## Remarks  
 The following table lists the possible return values for `GetCursorCommitBehavior` and the corresponding effect on the open recordset.  
  
|Return value|Effect on CRecordset objects|  
|------------------|----------------------------------|  
|`SQL_CB_CLOSE`|Call `CRecordset::Requery` immediately following the transaction commit.|  
|`SQL_CB_DELETE`|Call `CRecordset::Close` immediately following the transaction commit.|  
|`SQL_CB_PRESERVE`|Proceed normally with `CRecordset` operations.|  
  
 For more information about this return value, see the ODBC API function **SQLGetInfo** in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For more information about transactions, see the article [Transaction (ODBC)](../vs140/Transaction--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CDatabase Class](../vs140/CDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDatabase::GetCursorRollbackBehavior](../vs140/CDatabase--GetCursorRollbackBehavior.md)   
 [CDatabase::CanTransact](../vs140/CDatabase--CanTransact.md)   
 [CDatabase::BeginTrans](../vs140/CDatabase--BeginTrans.md)   
 [CDatabase::CommitTrans](../vs140/CDatabase--CommitTrans.md)   
 [CDatabase::Rollback](../vs140/CDatabase--Rollback.md)   
 [CRecordset Class](../vs140/CRecordset-Class.md)