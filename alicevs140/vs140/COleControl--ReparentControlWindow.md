---
title: "COleControl::ReparentControlWindow"
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
ms.assetid: 6eb4e7fc-c9ba-4e39-a2d5-74c901e1c8d9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::ReparentControlWindow
Sets the parent of the control.  
  
## Syntax  
  
```  
  
      virtual void ReparentControlWindow(  
   HWND hWndOuter,  
   HWND hWndParent  
);  
```  
  
#### Parameters  
 *hWndOuter*  
 The handle of the control window.  
  
 `hWndParent`  
 The handle of the new parent window.  
  
## Remarks  
 Call this function to reset the parent of the control window.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)