---
title: "COleControl::GetCapture"
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
ms.assetid: 0f8e63dc-db22-4be3-ada6-ea12e73186ac
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetCapture
Determines whether the `COleControl` object has the mouse capture.  
  
## Syntax  
  
```  
  
CWnd* GetCapture( );  
```  
  
## Return Value  
 If the control is activated and windowless, returns **this** if the control currently has the mouse capture (as determined by the control's container), or **NULL** if it does not have the capture.  
  
 Otherwise, returns the `CWnd` object that has the mouse capture (same as `CWnd::GetCapture`).  
  
## Remarks  
 An activated windowless control receives the mouse capture when [SetCapture](../vs140/COleControl--SetCapture.md) is called.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SetCapture](../vs140/COleControl--SetCapture.md)   
 [COleControl::ReleaseCapture](../vs140/COleControl--ReleaseCapture.md)