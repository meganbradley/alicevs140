---
title: "COleDocObjectItem::GetActiveView"
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
ms.assetid: 5257d290-66e6-4f91-8d8f-db3c8c53e1f6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocObjectItem::GetActiveView
Call this member function to get a pointer to the `IOleDocumentView` interface of the currently active view.  
  
## Syntax  
  
```  
  
LPOLEDOCUMENTVIEW GetActiveView( ) const;  
  
```  
  
## Return Value  
 A pointer to the [IOleDocumentView](http://msdn.microsoft.com/library/windows/desktop/ms678455) interface of the currently active view. If there is no current view, it returns **NULL**.  
  
## Remarks  
 The reference count on the returned `IOleDocumentView` pointer is not incremented before it is returned by this function.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocObjectItem Class](../vs140/COleDocObjectItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)