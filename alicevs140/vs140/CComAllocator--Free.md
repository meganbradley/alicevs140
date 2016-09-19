---
title: "CComAllocator::Free"
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
ms.assetid: 36f9fbbf-b230-41cb-a7f9-028f61855616
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAllocator::Free
Call this static function to free allocated memory.  
  
## Syntax  
  
```  
  
      static void Free(  
   void* p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 Pointer to the allocated memory.  
  
## Remarks  
 Frees the allocated memory. See [CoTaskMemFree](http://msdn.microsoft.com/library/windows/desktop/ms680722) for more details.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComAllocator Class](../vs140/CComAllocator-Class.md)   
 [CComAllocator::Allocate](../vs140/CComAllocator--Allocate.md)   
 [CComAllocator::Reallocate](../vs140/CComAllocator--Reallocate.md)