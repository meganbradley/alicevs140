---
title: "CWnd::IsDynamicLayoutEnabled"
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
ms.assetid: 4d318e34-3ecb-41d1-bd10-850f93525d67
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::IsDynamicLayoutEnabled
Determines whether dynamic layout is enabled on this window. If dynamic layout is enabled, the position and size of child windows can change when the user resizes the parent window.  
  
## Syntax  
  
```  
  
BOOL IsDynamicLayoutEnabled() const;  
  
```  
  
## Return Value  
 TRUE if dynamic layout is enabled; otherwise FALSE.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::EnableDynamicLayout](../vs140/CWnd--EnableDynamicLayout.md)   
 [CWnd::GetDynamicLayout](../vs140/CWnd--GetDynamicLayout.md)