---
title: "CWnd::GetParentFrame"
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
ms.assetid: a7954102-95b0-4d5a-9901-e533f19a07bf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetParentFrame
Call this member function to retrieve the parent frame window.  
  
## Syntax  
  
```  
  
CFrameWnd* GetParentFrame( ) const;  
```  
  
## Return Value  
 A pointer to a frame window if successful; otherwise **NULL**.  
  
## Remarks  
 The member function searches up the parent chain until a [CFrameWnd](../vs140/CFrameWnd-Class.md) (or derived class) object is found.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetDescendantWindow](../vs140/CWnd--GetDescendantWindow.md)   
 [CWnd::GetParent](../vs140/CWnd--GetParent.md)   
 [CFrameWnd::GetActiveView](../vs140/CFrameWnd--GetActiveView.md)