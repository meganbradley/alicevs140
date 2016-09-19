---
title: "CMFCVisualManagerOffice2003::SetUseGlobalTheme"
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
ms.assetid: e634dc37-d94e-4e9f-acf6-77f051ae2b9f
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::SetUseGlobalTheme
Specifies whether the visual manager uses a global theme.  
  
## Syntax  
  
```  
static void SetUseGlobalTheme(  
   BOOL bUseGlobalTheme = TRUE  
);  
```  
  
#### Parameters  
 [in] `bUseGlobalTheme`  
 `TRUE` if you want the visual manager to use a global theme; `FALSE` otherwise.  
  
## Remarks  
 If a `CMFCVisualManagerOffice2003` object uses a global theme, it draws the GUI elements by using the [CMFCVisualManagerWindows Class](../vs140/CMFCVisualManagerWindows-Class.md).  
  
 If a `CMFCVisualManagerOffice2003` object does not use a global theme, it draws the GUI elements by using the [CMFCVisualManagerOfficeXP Class](../vs140/CMFCVisualManagerOfficeXP-Class.md).  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCVisualManagerOfficeXP Class](../vs140/CMFCVisualManagerOfficeXP-Class.md)   
 [CMFCVisualManagerWindows Class](../vs140/CMFCVisualManagerWindows-Class.md)