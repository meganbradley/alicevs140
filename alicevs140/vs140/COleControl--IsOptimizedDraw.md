---
title: "COleControl::IsOptimizedDraw"
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
ms.assetid: cb09dc5c-b65f-4fa6-9117-2deff4bb31b6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::IsOptimizedDraw
Determines whether the container supports optimized drawing for the current drawing operation.  
  
## Syntax  
  
```  
  
BOOL IsOptimizedDraw( );  
```  
  
## Return Value  
 **TRUE** if the container supports optimized drawing for the current drawing operation; otherwise **FALSE**.  
  
## Remarks  
 If optimized drawing is supported, then the control need not select old objects (pens, brushes, fonts, etc.) into the device context when drawing is finished.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)