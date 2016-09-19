---
title: "COleClientItem::GetActiveView"
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
ms.assetid: c301e7df-60e9-4cc9-8d0c-f8f89aa5e1ab
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetActiveView
Returns the view on which the item is in-place activated.  
  
## Syntax  
  
```  
  
CView* GetActiveView( ) const;  
```  
  
## Return Value  
 A pointer to the view; otherwise **NULL** if the item is not in-place activated.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::IsInPlaceActive](../vs140/COleClientItem--IsInPlaceActive.md)   
 [COleClientItem::GetDocument](../vs140/COleClientItem--GetDocument.md)