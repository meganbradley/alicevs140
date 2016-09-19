---
title: "CRect::MoveToY"
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
ms.assetid: bcfcbed5-2ea6-446f-96d0-5192cd380678
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::MoveToY
Call this function to move the rectangle to the absolute y-coordinate specified by *y*.  
  
## Syntax  
  
```  
  
      void MoveToY(   
   int y    
) throw( );  
```  
  
#### Parameters  
 *y*  
 The absolute y-coordinate for the upper-left corner of the rectangle.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#48](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#48)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::MoveToXY](../vs140/CRect--MoveToXY.md)   
 [CRect::MoveToX](../vs140/CRect--MoveToX.md)