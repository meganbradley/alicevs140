---
title: "CDaoRecordset::GetLastModifiedBookmark"
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
ms.assetid: a7738bc3-a55c-47a1-abfc-ee25b79d8e3c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetLastModifiedBookmark
Call this member function to retrieve the bookmark of the most recently added or updated record.  
  
## Syntax  
  
```  
  
COleVariant GetLastModifiedBookmark( );  
  
```  
  
## Return Value  
 A `COleVariant` containing a bookmark that indicates the most recently added or changed record.  
  
## Remarks  
 When a recordset object is created or opened, each of its records already has a unique bookmark if it supports them. Call [GetBookmark](../vs140/CDaoRecordset--GetBookmark.md) to determine if the recordset supports bookmarks. If the recordset does not support bookmarks, a `CDaoException` is thrown.  
  
 When you add a record, it appears at the end of the recordset, and is not the current record. To make the new record current, call `GetLastModifiedBookmark` and then call `SetBookmark` to return to the newly added record.  
  
 For related information, see the topic "LastModified Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetBookmark](../vs140/CDaoRecordset--GetBookmark.md)   
 [CDaoRecordset::SetBookmark](../vs140/CDaoRecordset--SetBookmark.md)