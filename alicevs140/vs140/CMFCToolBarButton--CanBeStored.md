---
title: "CMFCToolBarButton::CanBeStored"
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
ms.assetid: 39b6ccf2-e05e-422d-b33d-e23ca0e446b6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::CanBeStored
Determines whether the button can be stored.  
  
## Syntax  
  
```  
virtual BOOL CanBeStored() const;  
```  
  
## Return Value  
 This method returns `TRUE`.  
  
## Remarks  
 The framework uses this method to determine whether the button can participate in a drag-and-drop operation.  
  
 The default implementation returns `TRUE`. Override this method if your button cannot be stored as part of a drag-and-drop operation. For more information about drag-and-drop operations, see [Drag and Drop (OLE)](../vs140/Drag-and-Drop--OLE-.md).  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Drag and Drop (OLE)](../vs140/Drag-and-Drop--OLE-.md)