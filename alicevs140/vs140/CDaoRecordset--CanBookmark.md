---
title: "CDaoRecordset::CanBookmark"
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
ms.assetid: e8c8bcd0-aa84-4b1e-84dd-5186605dcf59
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::CanBookmark
Call this member function to determine whether the previously opened recordset allows you to individually mark records using bookmarks.  
  
## Syntax  
  
```  
  
BOOL CanBookmark( );  
  
```  
  
## Return Value  
 Nonzero if the recordset supports bookmarks, otherwise 0.  
  
## Remarks  
 If you are using recordsets based entirely on Microsoft Jet database engine tables, bookmarks can be used except on snapshot-type recordsets flagged as forward-only scrolling recordsets. Other database products (external ODBC data sources) may not support bookmarks.  
  
 For related information, see the topic "Bookmarkable Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::CanAppend](../vs140/CDaoRecordset--CanAppend.md)   
 [CDaoRecordset::CanRestart](../vs140/CDaoRecordset--CanRestart.md)   
 [CDaoRecordset::CanScroll](../vs140/CDaoRecordset--CanScroll.md)   
 [CDaoRecordset::CanTransact](../vs140/CDaoRecordset--CanTransact.md)   
 [CDaoRecordset::CanUpdate](../vs140/CDaoRecordset--CanUpdate.md)