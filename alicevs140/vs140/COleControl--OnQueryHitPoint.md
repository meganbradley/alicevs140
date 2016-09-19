---
title: "COleControl::OnQueryHitPoint"
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
ms.assetid: 65c8f921-f7ee-4fce-a091-66c04741d3b4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnQueryHitPoint
Called by the framework in response to a container's **IViewObjectEx::QueryHitPoint** request.  
  
## Syntax  
  
```  
  
      virtual BOOL OnQueryHitPoint(  
   DWORD dwAspect,  
   LPCRECT pRectBounds,  
   POINT ptlLoc,  
   LONG lCloseHint,  
   DWORD* pHitResult   
);  
```  
  
#### Parameters  
 `dwAspect`  
 Specifies how the object is represented. Valid values are taken from the enumeration [DVASPECT](http://msdn.microsoft.com/library/windows/desktop/ms690318) or **DVASPECT2**.  
  
 `pRectBounds`  
 Pointer to a `RECT` structure specifying the bounding rectangle of the OLE control client area.  
  
 `ptlLoc`  
 Pointer to the **POINT** structure specifying the point to be checked for a hit. The point is specified in OLE client area coordinates.  
  
 `lCloseHint`  
 The distance that defines "close" to the point checked for a hit.  
  
 `pHitResult`  
 Pointer to the result of the hit query. One of the following values:  
  
-   **HITRESULT_OUTSIDE** `ptlLoc` is outside the OLE object and not close.  
  
-   **HITRESULT_TRANSPARENT** *ptlLoc* is within the bounds of the OLE object, but not close to the image. For example, a point in the middle of a transparent circle could be **HITRESULT_TRANSPARENT**.  
  
-   **HITRESULT_CLOSE** `ptlLoc` is inside or outside the OLE object but close enough to the object to be considered inside. Small, thin, or detailed objects may use this value. Even if a point is outside the bounding rectangle of an object it may still be close (this is needed for hitting small objects).  
  
-   **HITRESULT_HIT** `ptlLoc` is within the image of the object.  
  
## Return Value  
 Nonzero if a hit result is successfully returned; otherwise 0. A hit is an overlap with the OLE control display area.  
  
## Remarks  
 Queries whether an object's display rectangle overlaps the given point (hits the point). `QueryHitPoint` can be overridden to test hits for non-rectangular objects.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::OnQueryHitRect](../vs140/COleControl--OnQueryHitRect.md)