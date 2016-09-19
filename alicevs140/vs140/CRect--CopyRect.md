---
title: "CRect::CopyRect"
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
ms.assetid: af84c213-d6d0-47a2-ac68-1864f05e1905
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::CopyRect
Copies the `lpSrcRect` rectangle into `CRect`.  
  
## Syntax  
  
```  
  
      void CopyRect(   
   LPCRECT lpSrcRect    
) throw( );  
```  
  
#### Parameters  
 `lpSrcRect`  
 Points to the [RECT](../vs140/RECT-Structure.md) structure or `CRect` object that is to be copied.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#37](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#37)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::CRect](../vs140/CRect--CRect.md)   
 [CRect::operator =](../vs140/CRect--operator-=.md)   
 [CRect::SetRect](../vs140/CRect--SetRect.md)   
 [CRect::SetRectEmpty](../vs140/CRect--SetRectEmpty.md)