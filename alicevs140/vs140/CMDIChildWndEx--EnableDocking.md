---
title: "CMDIChildWndEx::EnableDocking"
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
ms.assetid: f07e843c-b89c-4971-91e7-4f86c79193af
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::EnableDocking
Enables docking of the child window to the main frame.  
  
## Syntax  
  
```  
BOOL EnableDocking(  
   DWORD dwDockStyle  
);  
```  
  
#### Parameters  
 [in] `dwDockStyle`  
 Specifies the docking alignment to enable.  
  
## Return Value  
 `TRUE` if the method succeeds; otherwise `FALSE`.  
  
## Remarks  
 Call this method to enable docking alignment to the main frame. You can pass a combination of CBRS_ALIGN_ flags (for more information, see [CControlBar::EnableDocking](../vs140/CControlBar--EnableDocking.md)).  
  
## Requirements  
 **Header:** afxmdichildwndex.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)