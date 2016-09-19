---
title: "CDaoRecordset::GetIndexCount"
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
ms.assetid: 2a259785-64ed-49d2-9746-a6b88118d500
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetIndexCount
Call this member function to determine the number of indexes available on the table-type recordset.  
  
## Syntax  
  
```  
  
short GetIndexCount( );  
  
```  
  
## Return Value  
 The number of indexes in the table-type recordset.  
  
## Remarks  
 `GetIndexCount` is useful for looping through all indexes in the recordset. For that purpose, use `GetIndexCount` in conjunction with [GetIndexInfo](../vs140/CDaoRecordset--GetIndexInfo.md). If you call this member function on dynaset-type or snapshot-type recordsets, MFC throws an exception.  
  
 For related information, see the topic "Attributes Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetFieldCount](../vs140/CDaoRecordset--GetFieldCount.md)   
 [CDaoRecordset::GetFieldInfo](../vs140/CDaoRecordset--GetFieldInfo.md)   
 [CDaoRecordset::GetIndexInfo](../vs140/CDaoRecordset--GetIndexInfo.md)