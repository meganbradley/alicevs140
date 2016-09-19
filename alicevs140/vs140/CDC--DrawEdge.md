---
title: "CDC::DrawEdge"
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
ms.assetid: e10d0fe1-f64d-4170-b38a-e0dd581cd5a3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::DrawEdge
Call this member function to draw the edges of a rectangle of the specified type and style.  
  
## Syntax  
  
```  
  
      BOOL DrawEdge(  
   LPRECT lpRect,  
   UINT nEdge,  
   UINT nFlags   
);  
```  
  
#### Parameters  
 `lpRect`  
 A pointer to a **RECT** structure that contains the logical coordinates of the rectangle.  
  
 *nEdge*  
 Specifies the type of inner and outer edge to draw. This parameter must be a combination of one inner-border flag and one outer-border flag. See [DrawEdge](http://msdn.microsoft.com/library/windows/desktop/dd162477) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a table of the parameter's types.  
  
 `nFlags`  
 The flags that specify the type of border to be drawn. See `DrawEdge` in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a table of the parameter's values. For diagonal lines, the **BF_RECT** flags specify the end point of the vector bounded by the rectangle parameter.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [DrawEdge](http://msdn.microsoft.com/library/windows/desktop/dd162477)