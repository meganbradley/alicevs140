---
title: "CWnd::PaintWindowlessControls"
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
ms.assetid: c745af88-93d9-46a4-93ed-e29d24cad5d4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::PaintWindowlessControls
Draws windowless controls on the control container.  
  
## Syntax  
  
```  
  
      BOOL PaintWindowlessControls(  
   CDC *pDC  
);  
```  
  
#### Parameters  
 `pDC`  
 The device context on which to draw the windowless controls.  
  
## Return Value  
 Returns TRUE if there is a control container and the windowless controls are drawn successfully, otherwise FALSE.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)