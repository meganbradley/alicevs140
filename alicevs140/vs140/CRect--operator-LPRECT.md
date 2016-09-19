---
title: "CRect::operator LPRECT"
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
ms.assetid: 628c15f5-113d-4416-a46d-64fb27bd3876
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::operator LPRECT
Converts a `CRect` to an [LPRECT](../vs140/Data-Types--MFC-.md).  
  
## Syntax  
  
```  
  
operator LPRECT( ) throw( );  
  
```  
  
## Remarks  
 When you use this function, you don't need the address-of (**&**) operator. This operator will be automatically used when you pass a `CRect` object to a function that expects an `LPRECT`.  
  
## Example  
 See the example for [CRect::operator LPCRECT](../vs140/CRect--operator-LPCRECT.md).  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::operator LPCRECT](../vs140/CRect--operator-LPCRECT.md)