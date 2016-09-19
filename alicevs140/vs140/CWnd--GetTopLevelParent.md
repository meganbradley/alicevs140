---
title: "CWnd::GetTopLevelParent"
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
ms.assetid: 3b5e5368-4614-4e6f-9bbd-8a0ae454265f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetTopLevelParent
Call this member function to retrieve the window's top-level parent.  
  
## Syntax  
  
```  
  
CWnd* GetTopLevelParent( ) const;  
  
```  
  
## Return Value  
 Identifies the top-level parent window of the window.  
  
 The returned pointer may be temporary and should not be stored for later use.  
  
## Remarks  
 `GetTopLevelParent` is similar to [GetTopLevelFrame](../vs140/CWnd--GetTopLevelFrame.md) and [GetTopLevelOwner](../vs140/CWnd--GetTopLevelOwner.md); however, it ignores the value set as the current owner window.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetTopLevelOwner](../vs140/CWnd--GetTopLevelOwner.md)   
 [CWnd::GetTopLevelFrame](../vs140/CWnd--GetTopLevelFrame.md)   
 [CWnd::GetOwner](../vs140/CWnd--GetOwner.md)   
 [CWnd::SetOwner](../vs140/CWnd--SetOwner.md)