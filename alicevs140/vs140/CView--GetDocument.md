---
title: "CView::GetDocument"
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
ms.assetid: 4587d385-aa2c-4341-90da-f1ae694f633b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CView::GetDocument
Call this function to get a pointer to the view's document.  
  
## Syntax  
  
```  
  
CDocument* GetDocument( ) const;  
```  
  
## Return Value  
 A pointer to the [CDocument](../vs140/CDocument-Class.md) object associated with the view. **NULL** if the view is not attached to a document.  
  
## Remarks  
 This allows you to call the document's member functions.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CView Class](../vs140/CView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument Class](../vs140/CDocument-Class.md)