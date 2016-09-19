---
title: "CDC::SelectClipPath"
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
ms.assetid: 6800f7d8-9726-4246-a9c4-93e850181a12
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SelectClipPath
Selects the current path as a clipping region for the device context, combining the new region with any existing clipping region by using the specified mode.  
  
## Syntax  
  
```  
  
      BOOL SelectClipPath(  
   int nMode   
);  
```  
  
#### Parameters  
 `nMode`  
 Specifies the way to use the path. The following values are allowed:  
  
-   **RGN_AND** The new clipping region includes the intersection (overlapping areas) of the current clipping region and the current path.  
  
-   **RGN_COPY** The new clipping region is the current path.  
  
-   **RGN_DIFF** The new clipping region includes the areas of the current clipping region, and those of the current path are excluded.  
  
-   **RGN_OR** The new clipping region includes the union (combined areas) of the current clipping region and the current path.  
  
-   **RGN_XOR** The new clipping region includes the union of the current clipping region and the current path, but without the overlapping areas.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The device context identified must contain a closed path.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::BeginPath](../vs140/CDC--BeginPath.md)   
 [CDC::EndPath](../vs140/CDC--EndPath.md)