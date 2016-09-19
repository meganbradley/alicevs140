---
title: "CMFCToolBar::SetCustomizeMode"
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
ms.assetid: 79cf3cee-cb0b-4bc0-bcab-799ede9ae720
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetCustomizeMode
Enables or disables customization mode for all toolbars in the application.  
  
## Syntax  
  
```  
static BOOL __stdcall SetCustomizeMode(  
   BOOL bSet=TRUE   
);  
```  
  
#### Parameters  
 [in] `bSet`  
 A Boolean value that specifies whether to enable or disable customization mode. Set this parameter to `TRUE` to enable customization mode or `FALSE` to disable it.  
  
## Return Value  
 `TRUE` if calling this method changes the customization mode; otherwise `FALSE`.  
  
## Remarks  
 This method adjusts the layout of and redraws each toolbar in the application. Call the [CMFCToolBar::IsCustomizeMode](../vs140/CMFCToolBar--IsCustomizeMode.md) method to determine whether the application is in customization mode,  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::IsCustomizeMode](../vs140/CMFCToolBar--IsCustomizeMode.md)