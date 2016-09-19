---
title: "CPoint::Offset"
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
ms.assetid: 6d103fc9-c570-4916-98d0-432aeae9216c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPoint::Offset
Adds values to the **x** and **y** members of the `CPoint`.  
  
## Syntax  
  
```  
  
      void Offset(  
   int xOffset,  
   int yOffset   
) throw( );  
void Offset(  
   POINT point   
) throw( );  
void Offset(  
   SIZE size   
) throw( );  
```  
  
#### Parameters  
 *xOffset*  
 Specifies the amount to offset the **x** member of the `CPoint`.  
  
 *yOffset*  
 Specifies the amount to offset the **y** member of the `CPoint`.  
  
 `point`  
 Specifies the amount ([POINT](../vs140/POINT-Structure.md) or `CPoint`) to offset the `CPoint`.  
  
 `size`  
 Specifies the amount ([SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) or [CSize](../vs140/CSize-Class.md)) to offset the `CPoint`.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#28](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#28)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CPoint Class](../vs140/CPoint-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPoint::operator +=](../vs140/CPoint--operator--=.md)   
 [CPoint::operator -=](../vs140/CPoint--operator--=.md)