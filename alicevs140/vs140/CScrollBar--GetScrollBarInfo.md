---
title: "CScrollBar::GetScrollBarInfo"
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
ms.assetid: 8a00d948-2268-48ab-a856-79f2586aef2e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollBar::GetScrollBarInfo
Retrieves the information that the **SCROLLBARINFO** structure maintains about a scroll bar.  
  
## Syntax  
  
```  
  
      BOOL GetScrollBarInfo(   
   PSCROLLBARINFO pScrollInfo    
) const;  
```  
  
#### Parameters  
 *pScrollInfo*  
 A pointer to the [SCROLLBARINFO](http://msdn.microsoft.com/library/windows/desktop/bb787535) structure.  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 This member function emulates the functionality of the [SBM_SCROLLBARINFO](http://msdn.microsoft.com/library/windows/desktop/bb787545) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollBar Class](../vs140/CScrollBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)