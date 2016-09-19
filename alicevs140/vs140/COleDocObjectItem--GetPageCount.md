---
title: "COleDocObjectItem::GetPageCount"
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
ms.assetid: 3c7299e7-1fa7-4ce2-96c9-291a15449f3f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocObjectItem::GetPageCount
Call this member function to retrieve the number of pages in the document.  
  
## Syntax  
  
```  
  
      BOOL GetPageCount(  
   LPLONG pnFirstPage,  
   LPLONG pcPages   
);  
```  
  
#### Parameters  
 *pnFirstPage*  
 A pointer to the number of the document's first page. Can be **NULL**, which indicates the caller doesn't need this number.  
  
 *pcPages*  
 A pointer to the total number of pages in the document. Can be **NULL**, which indicates the caller doesn't need this number.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocObjectItem Class](../vs140/COleDocObjectItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [IPrint::GetPageInfo](http://msdn.microsoft.com/library/windows/desktop/ms688632)