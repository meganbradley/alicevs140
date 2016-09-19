---
title: "AFX_GLOBAL_DATA::EnableAccessibilitySupport"
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
ms.assetid: 1b6af440-dc77-4da8-90fd-cadc842fdf16
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_GLOBAL_DATA::EnableAccessibilitySupport
Enables or disables Microsoft Active Accessibility support.  
  
## Syntax  
  
```  
void EnableAccessibilitySupport(  
   BOOL bEnable=TRUE   
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to enable accessibility support; `FALSE` to disable accessibility support. The default value is `TRUE`.  
  
## Remarks  
 Active Accessibility is a COM-based technology that improves the way programs and the Windows operating system work together with assistive technology products. It provides reliable methods for exposing information about user interface elements. However, a newer accessibility model called Microsoft UI Automation is now available. For a comparison of the two technologies, see [UI Automation and Microsoft Active Accessibility](assetId:///87bee662-0a3e-4232-a421-20e7a5968321).  
  
 Use the [AFX_GLOBAL_DATA::IsAccessibilitySupport](../vs140/AFX_GLOBAL_DATA--IsAccessibilitySupport.md) method to determine whether Microsoft Active Accessibility support is enabled.  
  
## Requirements  
 **Header:** afxglobals.h  
  
## See Also  
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [UI Automation and Microsoft Active Accessibility](assetId:///87bee662-0a3e-4232-a421-20e7a5968321)   
 [AFX_GLOBAL_DATA::IsAccessibilitySupport](../vs140/AFX_GLOBAL_DATA--IsAccessibilitySupport.md)