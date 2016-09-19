---
title: "CMFCToolBarButton::GetInvalidateRect"
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
ms.assetid: 95d365f9-f93a-4f3d-96f1-081e89d8279e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::GetInvalidateRect
Retrieves the region of the client area of the button that must be redrawn.  
  
## Syntax  
  
```  
virtual const CRect GetInvalidateRect() const;  
```  
  
## Return Value  
 A `CRect` object that specifies the region that must be redrawn.  
  
## Remarks  
 The default implementation of this method returns the whole client area. Override this method if you want a different area to be redrawn.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)