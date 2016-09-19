---
title: "CSocketAddr::GetAddrInfoList"
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
ms.assetid: 0e07dc4e-519f-4633-aa02-0e599750b9e8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSocketAddr::GetAddrInfoList
Call this method to return a pointer to the **addrinfo** list.  
  
## Syntax  
  
```  
  
addrinfo* const GetAddrInfoList( ) const;  
  
```  
  
## Return Value  
 Pointer to a linked list of one or more `addrinfo` structures containing response information about the host. For more information about the `addrinfo` structure, see the "addrinfo" article in the [MSDN Library](http://go.microsoft.com/fwlink/?linkid=556)  
  
## Requirements  
 **Header:** atlsocket.h  
  
## See Also  
 [CSocketAddr Class](../vs140/CSocketAddr-Class.md)   
 [CSocketAddr::GetAddrInfo](../vs140/CSocketAddr--GetAddrInfo.md)