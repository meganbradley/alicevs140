---
title: "AFX_GLOBAL_DATA::Resume"
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
ms.topic: article
ms.assetid: f7a2a311-5230-4348-963b-fb6f8ecb0f83
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_GLOBAL_DATA::Resume
Reinitializes internal function pointers that access methods that support Windows [themes and visual styles](_inet_themes_visualstyles_overview).  
  
## Syntax  
  
```  
BOOL Resume();  
```  
  
## Return Value  
 `TRUE` if this method succeeds; otherwise, `FALSE`. In debug mode, this method asserts if this method is unsuccessful.  
  
## Remarks  
 This method is called when the framework receives the [WM_POWERBROADCAST](http://msdn.microsoft.com/library/windows/desktop/aa373247) message.  
  
## Requirements  
 **Header:** afxglobals.h  
  
## See Also  
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [Themes and Visual Styles](_inet_themes_visualstyles_overview)