---
title: "CRect::SetRect"
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
ms.assetid: 09c60f9e-9df2-418a-9075-16b2a43d66e0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::SetRect
Sets the dimensions of `CRect` to the specified coordinates.  
  
## Syntax  
  
```  
  
      void SetRect(   
   int x1,   
   int y1,   
   int x2,   
   int y2    
) throw( );  
```  
  
#### Parameters  
 `x1`  
 Specifies the x-coordinate of the upper-left corner.  
  
 `y1`  
 Specifies the y-coordinate of the upper-left corner.  
  
 `x2`  
 Specifies the x-coordinate of the lower-right corner.  
  
 `y2`  
 Specifies the y-coordinate of the lower-right corner.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#52](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#52)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::CRect](../vs140/CRect--CRect.md)   
 [CRect::operator =](../vs140/CRect--operator-=.md)   
 [CRect::CopyRect](../vs140/CRect--CopyRect.md)   
 [CRect::SetRectEmpty](../vs140/CRect--SetRectEmpty.md)   
 [SetRect](http://msdn.microsoft.com/library/windows/desktop/dd145085)