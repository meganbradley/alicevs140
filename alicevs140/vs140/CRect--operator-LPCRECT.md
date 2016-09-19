---
title: "CRect::operator LPCRECT"
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
ms.assetid: 0c3849bd-6de7-4ee3-b4e8-427e2f640d0d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::operator LPCRECT
Converts a `CRect` to an [LPCRECT](../vs140/Data-Types--MFC-.md).  
  
## Syntax  
  
```  
  
operator LPCRECT( ) const throw( );  
  
```  
  
## Remarks  
 When you use this function, you don't need the address-of (**&**) operator. This operator will be automatically used when you pass a `CRect` object to a function that expects an **LPCRECT**.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#58](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#58)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::operator LPRECT](../vs140/CRect--operator-LPRECT.md)