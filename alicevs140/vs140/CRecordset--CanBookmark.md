---
title: "CRecordset::CanBookmark"
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
ms.assetid: 214e4025-83e2-4e52-aacd-37662a9942ca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::CanBookmark
Determines whether the recordset allows you to mark records using bookmarks.  
  
## Syntax  
  
```  
  
BOOL CanBookmark( ) const;  
  
```  
  
## Return Value  
 Nonzero if the recordset supports bookmarks; otherwise 0.  
  
## Remarks  
 This function is independent of the **CRecordset::useBookmarks** option in the `dwOptions` parameter of the [Open](../vs140/CRecordset--Open.md) member function. `CanBookmark` indicates whether the given ODBC driver and cursor type support bookmarks. **CRecordset::useBookmarks** indicates whether bookmarks will be available, provided they are supported.  
  
> [!NOTE]
>  Bookmarks are not supported on forward-only recordsets.  
  
 For more information about bookmarks and recordset navigation, see the articles [Recordset: Bookmarks and Absolute Positions (ODBC)](../vs140/Recordset--Bookmarks-and-Absolute-Positions--ODBC-.md) and [Recordset: Scrolling (ODBC)](../vs140/Recordset--Scrolling--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::GetBookmark](../vs140/CRecordset--GetBookmark.md)   
 [CRecordset::SetBookmark](../vs140/CRecordset--SetBookmark.md)