---
title: "COleControlContainer::ScrollChildren"
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
ms.assetid: bfda56da-4621-4601-89ed-fa45c101cbdb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::ScrollChildren
Called by the framework when scroll messages are received from a child window.  
  
## Syntax  
  
```  
  
      virtual void ScrollChildren(  
   int dx,  
   int dy   
);  
```  
  
#### Parameters  
 `dx`  
 The amount, in pixels, of scrolling along the x-axis.  
  
 *dy*  
 The amount, in pixels, of scrolling along the y-axis.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)