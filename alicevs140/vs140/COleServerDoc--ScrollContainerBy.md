---
title: "COleServerDoc::ScrollContainerBy"
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
ms.assetid: 9e15ae59-69b1-4bf5-8ae0-adaca68950e4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::ScrollContainerBy
Call the `ScrollContainerBy` member function to scroll the container document by the amount, in pixels, indicated by `sizeScroll`.  
  
## Syntax  
  
```  
  
      BOOL ScrollContainerBy(  
   CSize sizeScroll   
);  
```  
  
#### Parameters  
 `sizeScroll`  
 Indicates how far the container document is to scroll.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Positive values indicate scrolling down and to the right; negative values indicate scrolling up and to the left.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::OnScrollBy](../vs140/COleClientItem--OnScrollBy.md)