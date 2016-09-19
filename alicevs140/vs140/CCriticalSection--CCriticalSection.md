---
title: "CCriticalSection::CCriticalSection"
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
ms.assetid: 6a651c16-0a97-4fdf-bf29-e96def3e2425
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCriticalSection::CCriticalSection
Constructs a `CCriticalSection` object.  
  
## Syntax  
  
```  
  
CCriticalSection( );  
```  
  
## Remarks  
 To access or release a `CCriticalSection` object, create a [CSingleLock](../vs140/CSingleLock-Class.md) object and call its [Lock](../vs140/CSingleLock--Lock.md) and [Unlock](../vs140/CSingleLock--Unlock.md) member functions. If the `CCriticalSection` object is being used stand-alone, call its [Unlock](../vs140/CCriticalSection--Unlock.md) member function to release it.  
  
 If the constructor fails to allocate the required system memory, a memory exception (of type [CMemoryException](../vs140/CMemoryException-Class.md)) is automatically thrown.  
  
## Example  
 See the example for [CCriticalSection::Lock](../vs140/CCriticalSection--Lock.md).  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CCriticalSection Class](../vs140/CCriticalSection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)