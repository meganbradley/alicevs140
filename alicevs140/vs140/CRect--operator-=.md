---
title: "CRect::operator ="
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
ms.assetid: 02cf0c63-7ca4-4bfc-b113-440e7797360b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRect::operator =
Assigns *srcRect* to `CRect`.  
  
## Syntax  
  
```  
  
      void operator =(   
   const RECT& srcRect    
) throw( );  
```  
  
#### Parameters  
 *srcRect*  
 Refers to a source rectangle. Can be a [RECT](../vs140/RECT-Structure.md) or `CRect`.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#59](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#59)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CRect Class](../vs140/CRect-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::CRect](../vs140/CRect--CRect.md)   
 [CRect::SetRect](../vs140/CRect--SetRect.md)   
 [CRect::CopyRect](../vs140/CRect--CopyRect.md)   
 [CRect::SetRectEmpty](../vs140/CRect--SetRectEmpty.md)   
 [CopyRect](http://msdn.microsoft.com/library/windows/desktop/dd183481)