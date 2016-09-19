---
title: "CRect::MoveToXY"
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
ms.assetid: 6b3ff451-7bb6-452d-9722-90fa868c6c54
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::MoveToXY
Call this function to move the rectangle to the absolute x- and y-coordinates specified.  
  
## Syntax  
  
```  
  
      void MoveToXY(   
   int x,   
   int y    
) throw( );  
void MoveToXY(   
   POINT point    
) throw( );  
```  
  
#### Parameters  
 *x*  
 The absolute x-coordinate for the upper-left corner of the rectangle.  
  
 *y*  
 The absolute y-coordinate for the upper-left corner of the rectangle.  
  
 `point`  
 A **POINT** structure specifying the absolute upper-left corner of the rectangle.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#47](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#47)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::MoveToX](../vs140/CRect--MoveToX.md)   
 [CRect::MoveToY](../vs140/CRect--MoveToY.md)