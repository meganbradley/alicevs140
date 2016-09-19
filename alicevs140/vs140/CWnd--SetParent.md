---
title: "CWnd::SetParent"
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
ms.assetid: ffc43749-66ac-424b-8c26-92317384d9c4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SetParent
Changes the parent window of a child window.  
  
## Syntax  
  
```  
  
      CWnd* SetParent(  
   CWnd* pWndNewParent   
);  
```  
  
#### Parameters  
 *pWndNewParent*  
 Identifies the new parent window.  
  
## Return Value  
 A pointer to the previous parent window object if successful. The returned pointer may be temporary and should not be stored for later use.  
  
## Remarks  
 If the child window is visible, Windows performs the appropriate redrawing and repainting.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [SetParent](http://msdn.microsoft.com/library/windows/desktop/ms633541)   
 [CWnd::GetParent](../vs140/CWnd--GetParent.md)