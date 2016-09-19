---
title: "COleControl::OnSetObjectRects"
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
ms.assetid: 19a57b88-aa17-4e43-a7f5-aed4c226939a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnSetObjectRects
Called by the framework to implement a call to [IOleInPlaceObject::SetObjectRects](http://msdn.microsoft.com/library/windows/desktop/ms683767).  
  
## Syntax  
  
```  
  
      virtual BOOL OnSetObjectRects(  
   LPCRECT lpRectPos,  
   LPCRECT lpRectClip   
);  
```  
  
#### Parameters  
 *lpRectPos*  
 A pointer to a [RECT](../vs140/RECT-Structure.md) structure indicating the control's new position and size relative to the container.  
  
 `lpRectClip`  
 A pointer to a `RECT` structure indicating a rectangular area to which the control is to be clipped.  
  
## Return Value  
 Nonzero if the repositioning was accepted; otherwise 0.  
  
## Remarks  
 The default implementation automatically handles the repositioning and resizing of the control window and returns **TRUE**.  
  
 Override this function to alter the default behavior of this function.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)