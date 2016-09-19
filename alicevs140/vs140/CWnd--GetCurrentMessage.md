---
title: "CWnd::GetCurrentMessage"
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
ms.assetid: 3427f95d-9472-488b-b4a0-4b2d750cee12
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetCurrentMessage
Returns a pointer to the message this window is currently processing. Should only be called when in an **On***Message* message-handler member function.  
  
## Syntax  
  
```  
  
static const MSG* PASCAL GetCurrentMessage( );  
```  
  
## Return Value  
 Returns a pointer to the [MSG](../vs140/MSG-Structure.md) structure that contains the message the window is currently processing. Should only be called when in an **On***Message* handler.  
  
## Example  
 See the example for [CMDIFrameWnd::MDICascade](../vs140/CMDIFrameWnd--MDICascade.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)