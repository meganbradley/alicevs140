---
title: "CMFCToolBar::GetRowHeight"
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
ms.assetid: cfd5dfb3-4e8c-4758-a8e0-cd9923d759ca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetRowHeight
Returns the height of toolbar buttons.  
  
## Syntax  
  
```  
virtual int GetRowHeight() const;  
```  
  
## Return Value  
 The height of toolbar buttons, in pixels.  
  
## Remarks  
 The framework calls this method to calculate toolbar layout. Override this method in a derived class to specify a different height for your toolbar.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)