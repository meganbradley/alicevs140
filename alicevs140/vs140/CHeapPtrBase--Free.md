---
title: "CHeapPtrBase::Free"
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
ms.assetid: c8055123-2239-47c7-a408-dda1ae8809fa
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtrBase::Free
Call this method to delete an object pointed to by a `CHeapPtrBase`.  
  
## Syntax  
  
```  
  
void Free( ) throw( );  
  
```  
  
## Remarks  
 The object pointed to by the `CHeapPtrBase` is freed, and the [CHeapPtrBase::m_pData](../vs140/CHeapPtrBase--m_pData.md) member variable is set to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CHeapPtrBase Class](../vs140/CHeapPtrBase-Class.md)   
 [CHeapPtrBase::AllocateBytes](../vs140/CHeapPtrBase--AllocateBytes.md)   
 [CHeapPtrBase::ReallocateBytes](../vs140/CHeapPtrBase--ReallocateBytes.md)