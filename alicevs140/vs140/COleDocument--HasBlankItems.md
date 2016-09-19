---
title: "COleDocument::HasBlankItems"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: e5f46c97-ca56-4226-b742-f0882a416c25
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::HasBlankItems
Call this function to determine whether the document contains any blank items.  
  
## Syntax  
  
```  
  
BOOL HasBlankItems( ) const;  
```  
  
## Return Value  
 Nonzero if the document contains any blank items; otherwise 0.  
  
## Remarks  
 A blank item is one whose rectangle is empty.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocItem::IsBlank](../vs140/CDocItem--IsBlank.md)