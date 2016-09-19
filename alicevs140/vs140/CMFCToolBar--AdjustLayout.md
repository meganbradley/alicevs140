---
title: "CMFCToolBar::AdjustLayout"
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
ms.assetid: ecaabce2-ff27-49e6-8343-26d1b642e4cf
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::AdjustLayout
Recalculates the size and position of a toolbar.  
  
## Syntax  
  
```  
virtual void AdjustLayout();  
```  
  
## Remarks  
 Call this method when the toolbar has been created to recalculate its size and position.  
  
 The framework calls this method every time that the layout of the toolbar must be changed. For example, the layout must change when the user moves another control bar, resizes an application window, or customizes the toolbar.  
  
 Override this method to provide your own dynamic layout in classes that you derive from [CMFCToolar](../Topic/CMFCToolBar%20Class.md).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)