---
title: "CRecordset::IsDeleted"
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
ms.assetid: 45fbb3c3-6f3e-4775-8dce-cecbdf71af1e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::IsDeleted
Determines whether the current record has been deleted.  
  
## Syntax  
  
```  
  
BOOL IsDeleted( ) const;  
```  
  
## Return Value  
 Nonzero if the recordset is positioned on a deleted record; otherwise 0.  
  
## Remarks  
 If you scroll to a record and `IsDeleted` returns **TRUE** (nonzero), then you must scroll to another record before you can perform any other recordset operations.  
  
 The result of `IsDeleted` depends on many factors, such as your recordset type, whether your recordset is updatable, whether you specified the **CRecordset::skipDeletedRecords** option when you opened the recordset, whether your driver packs deleted records, and whether there are multiple users.  
  
 For more information about **CRecordset::skipDeletedRecords** and driver packing, see the [Open](../vs140/CRecordset--Open.md) member function.  
  
> [!NOTE]
>  If you have implemented bulk row fetching, you should not call `IsDeleted`. Instead, call the [GetRowStatus](../vs140/CRecordset--GetRowStatus.md) member function. For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::Delete](../vs140/CRecordset--Delete.md)   
 [CRecordset::IsBOF](../vs140/CRecordset--IsBOF.md)   
 [CRecordset::IsEOF](../vs140/CRecordset--IsEOF.md)   
 [CRecordset::Move](../vs140/CRecordset--Move.md)