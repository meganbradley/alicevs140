---
title: "CHeapPtr::CHeapPtr"
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
ms.assetid: 491b5eb8-6db1-4957-ba9b-d213759686de
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtr::CHeapPtr
The constructor.  
  
## Syntax  
  
```  
  
      CHeapPtr( ) throw( );   
explicit CHeapPtr(  
   T* p   
) throw( );  
CHeapPtr(  
   CHeapPtr< T, Allocator >& p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 An existing heap pointer or `CHeapPtr`.  
  
## Remarks  
 The heap pointer can optionally be created using an existing pointer, or a `CHeapPtr` object. If so, the new `CHeapPtr` object assumes responsibility for managing the new pointer and resources.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#78](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#78)]  
  
## Requirements  
 **Header:** atlalloc.h  
  
## See Also  
 [CHeapPtr Class](../vs140/CHeapPtr-Class.md)