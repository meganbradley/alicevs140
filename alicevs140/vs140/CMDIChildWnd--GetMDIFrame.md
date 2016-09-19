---
title: "CMDIChildWnd::GetMDIFrame"
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
ms.assetid: 575acb86-4082-4c28-b863-db4b6dafb051
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWnd::GetMDIFrame
Call this function to return the MDI parent frame.  
  
## Syntax  
  
```  
  
CMDIFrameWnd* GetMDIFrame( );  
```  
  
## Return Value  
 A pointer to the MDI parent frame window.  
  
## Remarks  
 The frame returned is two parents removed from the `CMDIChildWnd` and is the parent of the window of type **MDICLIENT** that manages the `CMDIChildWnd` object. Call the [GetParent](../vs140/CWnd--GetParent.md) member function to return the `CMDIChildWnd` object's immediate **MDICLIENT** parent as a temporary `CWnd` pointer.  
  
## Example  
 See the example for [CMDIFrameWnd::MDISetMenu](../vs140/CMDIFrameWnd--MDISetMenu.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMDIChildWnd Class](../vs140/CMDIChildWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetParent](../vs140/CWnd--GetParent.md)