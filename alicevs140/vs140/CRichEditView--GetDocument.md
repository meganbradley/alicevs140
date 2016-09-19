---
title: "CRichEditView::GetDocument"
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
ms.assetid: 318f6b2f-1523-41a3-9c16-87fea82b43fe
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::GetDocument
Call this function to get a pointer to the `CRichEditDoc` associated with this view.  
  
## Syntax  
  
```  
  
CRichEditDoc* GetDocument( ) const;  
  
```  
  
## Return Value  
 Pointer to a [CRichEditDoc](../vs140/CRichEditDoc-Class.md) object associated with your `CRichEditView` object.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditDoc Class](../vs140/CRichEditDoc-Class.md)   
 [CView::GetDocument](../vs140/CView--GetDocument.md)   
 [COleClientItem::GetDocument](../vs140/COleClientItem--GetDocument.md)