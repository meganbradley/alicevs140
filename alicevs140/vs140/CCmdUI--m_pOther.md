---
title: "CCmdUI::m_pOther"
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
ms.assetid: 7c79ced0-a4df-45b4-b63b-00ee738d91b8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdUI::m_pOther
Pointer (of type `CWnd`) to the window object, such as a tool or status bar, that sent the notification.  
  
## Syntax  
  
```  
  
CWnd* m_pOther;  
  
```  
  
## Remarks  
 **NULL** if the item is a menu or a non-`CWnd` object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdUI Class](../vs140/CCmdUI-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd Class](../vs140/CWnd-Class.md)