---
title: "COleControl::ReleaseCapture"
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
ms.assetid: 57555bc0-6a01-43f2-9932-ac1e164e1967
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::ReleaseCapture
Releases mouse capture.  
  
## Syntax  
  
```  
  
BOOL ReleaseCapture( );  
```  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 If the control currently has the mouse capture, the capture is released. Otherwise, this function has no effect.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SetCapture](../vs140/COleControl--SetCapture.md)   
 [COleControl::GetCapture](../vs140/COleControl--GetCapture.md)