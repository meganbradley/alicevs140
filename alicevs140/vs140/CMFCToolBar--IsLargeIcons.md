---
title: "CMFCToolBar::IsLargeIcons"
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
ms.assetid: ac335dc2-f1d8-4a5d-95dc-a21e57153c40
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::IsLargeIcons
Specifies whether toolbars in the application currently display large icons.  
  
## Syntax  
  
```  
static BOOL IsLargeIcons();  
```  
  
## Return Value  
 `TRUE` if the application is using large icons; otherwise `FALSE`.  
  
## Remarks  
 Call [CMFCToolBar::SetLargeIcons](../vs140/CMFCToolBar--SetLargeIcons.md) to toggle between large icons and regular icons.  
  
 The framework automatically changes the mode when the user toggles the **Large icons** check-box on the **Options** page of the **Customization** dialog box.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)