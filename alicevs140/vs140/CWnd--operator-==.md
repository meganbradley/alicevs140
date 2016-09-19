---
title: "CWnd::operator =="
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
ms.assetid: f0c3c783-5812-4aad-a07b-b041ea33657d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::operator ==
Compares two `CWnd` objects to determine if they have the same [m_hWnd](../vs140/CWnd--m_hWnd.md).  
  
## Syntax  
  
```  
  
      BOOL operator==(  
   const CWnd& wnd   
) const;  
```  
  
#### Parameters  
 `wnd`  
 A reference to a `CWnd` object.  
  
## Return Value  
 Nonzero if equal; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::operator !=](../vs140/CWnd--operator-!=.md)