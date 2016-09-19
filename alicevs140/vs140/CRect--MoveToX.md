---
title: "CRect::MoveToX"
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
ms.assetid: e1708247-0473-4545-9a52-aca7813e127b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::MoveToX
Call this function to move the rectangle to the absolute x-coordinate specified by *x*.  
  
## Syntax  
  
```  
  
      void MoveToX(   
   int x    
) throw( );  
```  
  
#### Parameters  
 *x*  
 The absolute x-coordinate for the upper-left corner of the rectangle.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#46](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#46)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::MoveToXY](../vs140/CRect--MoveToXY.md)   
 [CRect::MoveToY](../vs140/CRect--MoveToY.md)