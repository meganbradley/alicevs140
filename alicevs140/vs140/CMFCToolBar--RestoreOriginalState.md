---
title: "CMFCToolBar::RestoreOriginalState"
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
ms.assetid: 41eb2fea-890c-46fe-b393-c70e67ad1b88
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::RestoreOriginalState
Restores the original state of a toolbar.  
  
## Syntax  
  
```  
virtual BOOL RestoreOriginalState();  
```  
  
## Return Value  
 `TRUE` if the method succeeds, or `FALSE` if the method fails or the toolbar is user-defined.  
  
## Remarks  
 This method loads the toolbar from the resource file by using the [CMFCToolBar::LoadToolBar](../vs140/CMFCToolBar--LoadToolBar.md) method.  
  
 The framework calls this method when the user chooses the **Reset All** button on the **Toolbars** page of a customization dialog box.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::LoadToolBar](../vs140/CMFCToolBar--LoadToolBar.md)