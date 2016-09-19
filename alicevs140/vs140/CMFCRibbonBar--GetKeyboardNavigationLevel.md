---
title: "CMFCRibbonBar::GetKeyboardNavigationLevel"
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
ms.assetid: 6f535c77-a97b-41d9-8d1d-7caf6698c19a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::GetKeyboardNavigationLevel
Retrieves the current navigation level as the user presses the keytips that are contained on the ribbon bar.  
  
## Syntax  
  
```  
int GetKeyboardNavigationLevel() const;  
```  
  
## Return Value  
 The current navigation level as the user presses the keytips that are contained on the ribbon bar. The following table lists possible return values:  
  
 -1  
 Keytips are not displayed.  
  
 0  
 Keytips are displayed.  
  
 1  
 User has pressed a displayed keytip.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)