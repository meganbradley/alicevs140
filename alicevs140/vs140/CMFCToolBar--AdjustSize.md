---
title: "CMFCToolBar::AdjustSize"
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
ms.assetid: 0d157738-fe0d-4e90-b12a-c6cf7a0529fa
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::AdjustSize
Recalculates the size of the toolbar.  
  
## Syntax  
  
```  
void AdjustSize();  
```  
  
## Remarks  
 This method makes sure that the toolbar fits in the bounds of the parent frame. This method does nothing if the toolbar has no parent frame.  
  
 The [CMFCToolBar::AdjustLayout](../vs140/CMFCToolBar--AdjustLayout.md) method calls this method to recalculate the size if the parent of the toolbar is not a `CMFCReBar` object.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::AdjustLayout](../vs140/CMFCToolBar--AdjustLayout.md)   
 [CMFCReBar Class](../vs140/CMFCReBar-Class.md)