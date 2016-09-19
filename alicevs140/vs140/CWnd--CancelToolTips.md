---
title: "CWnd::CancelToolTips"
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
ms.assetid: 55bbf7c6-124d-4f2e-84b6-a183a2897e15
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::CancelToolTips
Call this member function to remove a tool tip from the screen if a tool tip is currently displayed.  
  
## Syntax  
  
```  
  
      static void PASCAL CancelToolTips(  
   BOOL bKeys = FALSE   
);  
```  
  
#### Parameters  
 *bKeys*  
 **TRUE** to cancel tool tips when a key is pressed and set the status bar text to the default; otherwise **FALSE**.  
  
## Remarks  
  
> [!NOTE]
>  Using this member function has no effect on tool tips managed by your code. It only affects the tool tip control managed by [CWnd::EnableToolTips](../vs140/CWnd--EnableToolTips.md).  
  
## Example  
 [!CODE [NVC_MFCWindowing#73](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#73)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::EnableToolTips](../vs140/CWnd--EnableToolTips.md)   
 [TTM_ACTIVATE](http://msdn.microsoft.com/library/windows/desktop/bb760326)