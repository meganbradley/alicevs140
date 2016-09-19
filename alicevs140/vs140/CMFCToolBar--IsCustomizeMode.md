---
title: "CMFCToolBar::IsCustomizeMode"
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
ms.assetid: 01f909c9-637a-4fd5-be29-981185b1e1fc
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::IsCustomizeMode
Specifies whether the toolbar framework is in customization mode.  
  
## Syntax  
  
```  
static BOOL IsCustomizeMode();  
```  
  
## Return Value  
 `TRUE` if the framework is in customization mode; otherwise `FALSE`.  
  
## Remarks  
 You can toggle customization mode by calling [CMFCToolBar::SetCustomizeMode](../vs140/CMFCToolBar--SetCustomizeMode.md).  
  
 The framework changes the mode when the user invokes the customization dialog box ([CMFCToolBarsCustomizeDialog](../vs140/CMFCToolBarsCustomizeDialog-Class.md)).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)