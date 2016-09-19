---
title: "CMFCButton::EnableWindowsTheming"
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
ms.assetid: b43dda18-657d-4601-930b-e2e82e43e954
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCButton::EnableWindowsTheming
Specifies whether the style of the button border corresponds to the current Windows theme.  
  
## Syntax  
  
```  
static void EnableWindowsTheming(  
   BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to use the current Windows theme to draw button borders; `FALSE` to not use the Windows theme. The default is `TRUE`.  
  
## Remarks  
 This method affects all buttons in your application that are derived from the `CMFCButton` class.  
  
## Requirements  
 **Header:** afxbutton.h  
  
## See Also  
 [CMFCButton Class](../vs140/CMFCButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCButton::IsWindowsThemingEnabled](../vs140/CMFCButton--IsWindowsThemingEnabled.md)