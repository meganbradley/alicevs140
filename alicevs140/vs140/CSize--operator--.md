---
title: "CSize::operator -"
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
ms.assetid: 45a2e93d-b338-4f4b-b17c-f548cc789edb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSize::operator -
The first three of these operators subtract this `CSize` value to the value of parameter.  
  
## Syntax  
  
```  
  
      CSize operator -(   
   SIZE size    
) const throw( );  
CPoint operator -(   
   POINT point    
) const throw( );  
CRect operator -(   
   const RECT* lpRect    
) const throw( );  
CSize operator -( ) const throw( );  
```  
  
## Remarks  
 The fourth operator, the unary minus, changes the sign of the `CSize` value. See the following descriptions of the individual operators:  
  
-   **operator -(**  `size`  **)** This operation subtracts two `CSize` values.  
  
-   **operator -(**  `point`  **)** This operation offsets (moves) a [POINT](http://msdn.microsoft.com/library/windows/desktop/dd162805) or [CPoint](../vs140/CPoint-Class.md) value by the additive inverse of this `CSize` value. The **cx** and **cy** of this `CSize` value are subtracted from the **x** and **y** data members of the **POINT** value. It is analogous to the version of [CPoint::operator -](../vs140/CPoint--operator--.md) that takes a [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) parameter.  
  
-   **operator -(**  `lpRect`  **)** This operation offsets (moves) a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) or [CRect](../vs140/CRect-Class.md) value by the additive inverse of this `CSize` value. The **cx** and **cy** members of this `CSize` value are subtracted from the **left**, **top**, **right**, and **bottom** data members of the `RECT` value. It is analogous to the version of [CRect::operator -](../vs140/CRect--operator--.md) that takes a [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) parameter.  
  
-   **operator -( )** This operation returns the additive inverse of this `CSize` value.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#103](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#103)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CSize Class](../vs140/CSize-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPoint::operator -](../vs140/CPoint--operator--.md)   
 [CRect::operator -](../vs140/CRect--operator--.md)