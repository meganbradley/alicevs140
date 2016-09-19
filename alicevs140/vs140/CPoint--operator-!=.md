---
title: "CPoint::operator !="
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
ms.assetid: 7d94f119-4e4d-4c77-bcc7-8d54d3b84c8f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPoint::operator !=
Checks for inequality between two points.  
  
## Syntax  
  
```  
  
      BOOL operator!=(  
   POINT point   
) const throw( );  
```  
  
#### Parameters  
 `point`  
 Contains a [POINT](../vs140/POINT-Structure.md) structure or `CPoint` object.  
  
## Return Value  
 Nonzero if the points are not equal; otherwise 0.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#30](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#30)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CPoint Class](../vs140/CPoint-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPoint::operator ==](../vs140/CPoint--operator-==.md)