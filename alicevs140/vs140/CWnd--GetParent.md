---
title: "CWnd::GetParent"
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
ms.assetid: fe43ff8c-f534-4c59-aedb-2481f4a7743a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetParent
Call this function to get a pointer to a child window's parent window (if any).  
  
## Syntax  
  
```  
  
CWnd* GetParent( ) const;  
```  
  
## Return Value  
 See the Return Values section in [GetParent](http://msdn.microsoft.com/library/windows/desktop/ms633510) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 The `GetParent` function returns a pointer to the immediate parent (if it exists). In contrast, the [GetParentOwner](../vs140/CWnd--GetParentOwner.md) function returns a pointer to the most immediate parent or owner window that is not a child window (does not have the **WS_CHILD** style). If you have a child window within a child window `GetParent` and `GetParentOwner` return different results.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetAncestor](../vs140/CWnd--GetAncestor.md)   
 [CWnd::GetParentOwner](../vs140/CWnd--GetParentOwner.md)   
 [CWnd::GetOwner](../vs140/CWnd--GetOwner.md)   
 [CWnd::SetOwner](../vs140/CWnd--SetOwner.md)   
 [CWnd::SetParent](../vs140/CWnd--SetParent.md)   
 [GetParent](http://msdn.microsoft.com/library/windows/desktop/ms633510)