---
title: "CDaoRecordset::GetBookmark"
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
ms.assetid: 418560be-dd2d-4bd7-b067-36fbca010a0f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetBookmark
Call this member function to obtain the bookmark value in a particular record.  
  
## Syntax  
  
```  
  
COleVariant GetBookmark( );  
  
```  
  
## Return Value  
 Returns a value representing the bookmark on the current record.  
  
## Remarks  
 When a recordset object is created or opened, each of its records already has a unique bookmark if it supports them. Call `CanBookmark` to determine whether a recordset supports bookmarks.  
  
 You can save the bookmark for the current record by assigning the value of the bookmark to a `COleVariant` object. To quickly return to that record at any time after moving to a different record, call `SetBookmark` with a parameter corresponding to the value of that `COleVariant` object.  
  
> [!NOTE]
>  Calling [Requery](../vs140/CDaoRecordset--Requery.md) changes DAO bookmarks.  
  
 For related information, see the topic "Bookmark Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::SetBookmark](../vs140/CDaoRecordset--SetBookmark.md)   
 [CDaoRecordset::CanBookmark](../vs140/CDaoRecordset--CanBookmark.md)