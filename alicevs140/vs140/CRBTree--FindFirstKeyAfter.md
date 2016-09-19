---
title: "CRBTree::FindFirstKeyAfter"
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
ms.assetid: 9bb15150-5505-4dff-9b31-3547acb8403b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::FindFirstKeyAfter
Call this method to find the position of the element that uses the next available key.  
  
## Syntax  
  
```  
  
      POSITION FindFirstKeyAfter(  
   KINARGTYPE key   
) const throw( );  
```  
  
#### Parameters  
 `key`  
 A key value.  
  
## Return Value  
 Returns the position value of the element that uses the next available key. If there are no more elements, NULL is returned.  
  
## Remarks  
 This method makes it easy to traverse the tree without having to calculate position values beforehand.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)