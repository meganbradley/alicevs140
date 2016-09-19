---
title: "COleControl::TransformCoords"
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
ms.assetid: c7c162e5-ca40-494c-9cc2-5a85c272385a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::TransformCoords
Transforms coordinate values between **HIMETRIC** units and the container's native units.  
  
## Syntax  
  
```  
  
      void TransformCoords(  
   POINTL* lpptlHimetric,  
   POINTF* lpptfContainer,  
   DWORD flags   
);  
```  
  
#### Parameters  
 *lpptlHimetric*  
 Pointer to a **POINTL** structure containing coordinates in **HIMETRIC** units.  
  
 *lpptfContainer*  
 Pointer to a **POINTF** structure containing coordinates in the container's unit size.  
  
 `flags`  
 A combination of the following values:  
  
-   **XFORMCOORDS_POSITION** A position in the container.  
  
-   **XFORMCOORDS_SIZE** A size in the container.  
  
-   **XFORMCOORDS_HIMETRICTOCONTAINER** Transform **HIMETRIC** units to the container's units.  
  
-   **XFORMCOORDS_CONTAINERTOHIMETRIC** Transform the container's units to **HIMETRIC** units.  
  
## Remarks  
 The first two flags, **XFORMCOORDS_POSITION** and **XFORMCOORDS_SIZE**, indicate whether the coordinates should be treated as a position or a size. The remaining two flags indicate the direction of transformation.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::AmbientScaleUnits](../vs140/COleControl--AmbientScaleUnits.md)