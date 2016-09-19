---
title: "CCriticalSection::Lock"
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
ms.assetid: 9d3e0ee9-4626-487f-b88f-1937a7a49e1f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCriticalSection::Lock
Call this member function to gain access to the critical section object.  
  
## Syntax  
  
```  
  
      BOOL Lock( );   
BOOL Lock(  
   DWORD dwTimeout   
);  
```  
  
#### Parameters  
 `dwTimeout`  
 `Lock` ignores this parameter value.  
  
## Return Value  
 Nonzero if the function was successful; otherwise 0.  
  
## Remarks  
 `Lock` is a blocking call that will not return until the critical section object is signaled (becomes available).  
  
 If timed waits are necessary, you can use a [CMutex](../vs140/CMutex-Class.md) object instead of a `CCriticalSection` object.  
  
 If `Lock` fails to allocate the necessary system memory, a memory exception (of type [CMemoryException](../vs140/CMemoryException-Class.md)) is automatically thrown.  
  
## Example  
 This example demonstrates the nested critical section approach by controlling access to a shared resource (the static `_strShared` object) using a shared `CCriticalSection` object. The `SomeMethod` function demonstrates updating a shared resource in a safe manner.  
  
 [!CODE [NVC_MFC_Utilities#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#11)]  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CCriticalSection Class](../vs140/CCriticalSection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSingleLock::Lock](../vs140/CSingleLock--Lock.md)