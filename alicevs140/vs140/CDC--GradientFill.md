---
title: "CDC::GradientFill"
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
ms.assetid: 934ed8c3-35f5-40fb-98bd-6919acff262b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GradientFill
Call this member function to fill rectangle and triangle structures with color that smoothly fades from one side to the other.  
  
## Syntax  
  
```  
  
      BOOL GradientFill(  
   TRIVERTEX* pVertices,  
   ULONG nVertices,  
   void* pMesh,  
   ULONG nMeshElements,  
   DWORD dwMode   
);  
```  
  
#### Parameters  
 *pVertices*  
 Pointer to an array of [TRIVERTEX](http://msdn.microsoft.com/library/windows/desktop/dd145142) structures that each define a triangle vertex.  
  
 *nVertices*  
 The number of vertices.  
  
 `pMesh`  
 Array of [GRADIENT_TRIANGLE](http://msdn.microsoft.com/library/windows/desktop/dd144959) structures in triangle mode, or an array of [GRADIENT_RECT](http://msdn.microsoft.com/library/windows/desktop/dd144958) structures in rectangle mode.  
  
 *nMeshElements*  
 The number of elements (triangles or rectangles) in `pMesh`.  
  
 `dwMode`  
 Specifies gradient fill mode. For a list of possible values, see [GradientFill](http://msdn.microsoft.com/library/windows/desktop/dd144957) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 **TRUE** if successful; otherwise **FALSE**.  
  
## Remarks  
 For more information, see `GradientFill` in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [EMRGRADIENTFILL](http://msdn.microsoft.com/library/windows/desktop/dd162542)