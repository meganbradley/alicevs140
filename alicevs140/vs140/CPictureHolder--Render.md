---
title: "CPictureHolder::Render"
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
ms.assetid: f1af1863-72bf-4020-ac45-a15f0eb61fe0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPictureHolder::Render
Renders the picture in the rectangle referenced by `rcRender`.  
  
## Syntax  
  
```  
  
      void Render(  
   CDC* pDC,  
   const CRect& rcRender,  
   const CRect& rcWBounds   
);  
```  
  
#### Parameters  
 `pDC`  
 Pointer to the display context in which the picture is to be rendered.  
  
 `rcRender`  
 Rectangle in which the picture is to be rendered.  
  
 *rcWBounds*  
 A rectangle representing the bounding rectangle of the object rendering the picture. For a control, this rectangle is the `rcBounds` parameter passed to an override of [COleControl::OnDraw](../vs140/COleControl--OnDraw.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPictureHolder Class](../vs140/CPictureHolder-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)