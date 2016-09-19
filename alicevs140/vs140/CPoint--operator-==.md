---
title: "CPoint::operator =="
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
ms.assetid: f9e8b9d7-fab2-40ff-976a-696959cd282e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPoint::operator ==
Checks for equality between two points.  
  
## Syntax  
  
```  
  
      BOOL operator ==(  
   POINT point   
) const throw( );  
```  
  
#### Parameters  
 `point`  
 Contains a [POINT](../vs140/POINT-Structure.md) structure or `CPoint` object.  
  
## Return Value  
 Nonzero if the points are equal; otherwise 0.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#29](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#29)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CPoint Class](../vs140/CPoint-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPoint::operator !=](../vs140/CPoint--operator-!=.md)