---
title: "CMDIChildWnd::SetHandles"
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
ms.assetid: d868714e-909e-49f7-972a-6f8927be3df4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWnd::SetHandles
Sets the handles for menu and accelerator resources.  
  
## Syntax  
  
```  
  
      void SetHandles(  
   HMENU hMenu,  
   HACCEL hAccel  
);  
```  
  
#### Parameters  
 `hMenu`  
 The handle of a menu resource.  
  
 `hAccel`  
 The handle of an accelerator resource.  
  
## Remarks  
 Call this function to set the menu and accelerator resources used by the MDI child window object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIChildWnd Class](../vs140/CMDIChildWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)