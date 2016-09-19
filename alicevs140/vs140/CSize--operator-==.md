---
title: "CSize::operator =="
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
ms.assetid: ed3dd218-ecec-43b7-bcbb-1852c938dfe3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSize::operator ==
Checks for equality between two sizes.  
  
## Syntax  
  
```  
  
      BOOL operator ==(   
   SIZE size    
) const throw( );  
```  
  
## Remarks  
 Returns nonzero if the sizes are equal, otherwize 0.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#98](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#98)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CSize Class](../vs140/CSize-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSize::operator !=](../vs140/CSize--operator-!=.md)