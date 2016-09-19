---
title: "CSocketAddr::GetAddrInfo"
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
ms.assetid: b4875d55-71c1-46a9-aa66-42a62b17b0ce
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSocketAddr::GetAddrInfo
Call this method to return a pointer to a specific element in the **addrinfo** list.  
  
## Syntax  
  
```  
  
      addrinfo* const GetAddrInfo(   
   int nIndex = 0  
) const;  
```  
  
#### Parameters  
 `nIndex`  
 A reference to a specific element in the [addrinfo](http://msdn.microsoft.com/library/windows/desktop/ms737530) list.  
  
## Return Value  
 Returns a pointer to the **addrinfo** structure referenced by `nIndex` in the linked list containing response information about the host.  
  
## Requirements  
 **Header:** atlsocket.h  
  
## See Also  
 [CSocketAddr Class](../vs140/CSocketAddr-Class.md)   
 [CSocketAddr::GetAddrInfoList](../vs140/CSocketAddr--GetAddrInfoList.md)