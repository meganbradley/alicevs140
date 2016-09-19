---
title: "CControlBar::IsFloating"
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
ms.assetid: ca5a2b35-9a68-4bea-8cf3-9b655c0d47b1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CControlBar::IsFloating
Call this member function to determine whether the control bar is floating or docked.  
  
## Syntax  
  
```  
  
BOOL IsFloating( ) const;  
  
```  
  
## Return Value  
 Nonzero if the control bar is floating; otherwise 0.  
  
## Remarks  
 To change the state of a control bar from docked to floating, call [CFrameWnd::FloatControlBar](../vs140/CFrameWnd--FloatControlBar.md).  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CControlBar Class](../vs140/CControlBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::FloatControlBar](../vs140/CFrameWnd--FloatControlBar.md)