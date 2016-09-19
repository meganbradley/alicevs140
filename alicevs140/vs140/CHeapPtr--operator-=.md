---
title: "CHeapPtr::operator ="
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
ms.assetid: db730734-606a-434a-a892-dcf1ae867c49
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtr::operator =
Assignment operator.  
  
## Syntax  
  
```  
  
      CHeapPtr< T, Allocator >& operator =(  
   CHeapPtr< T, Allocator >& p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 An existing `CHeapPtr` object.  
  
## Return Value  
 Returns a reference to the updated `CHeapPtr`.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#80](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#80)]  
  
## Requirements  
 **Header:** atlalloc.h  
  
## See Also  
 [CHeapPtr Class](../vs140/CHeapPtr-Class.md)