---
title: "CMFCToolBarButton::OnClickUp"
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
ms.assetid: 6268e9c6-cdbd-48d8-a7a3-b3eb3f279577
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::OnClickUp
Called by the framework when the user releases the mouse button.  
  
## Syntax  
  
```  
virtual BOOL OnClickUp();  
```  
  
## Return Value  
 This method returns `FALSE`.  
  
## Remarks  
 The framework calls this method when the user releases the toolbar button.  
  
 The default implementation does nothing and returns `FALSE`. Override this method to return a nonzero value if the button processes the click message.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)