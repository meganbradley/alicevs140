---
title: "CSocket::FromHandle"
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
ms.assetid: b48ab8d0-a99f-4201-a223-bdb73d5bdde3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSocket::FromHandle
Returns a pointer to a `CSocket` object.  
  
## Syntax  
  
```  
  
      static CSocket* PASCAL FromHandle(  
   SOCKET hSocket   
);  
```  
  
#### Parameters  
 `hSocket`  
 Contains a handle to a socket.  
  
## Return Value  
 A pointer to a `CSocket` object, or **NULL** if there is no `CSocket` object attached to `hSocket`.  
  
## Remarks  
 When given a **SOCKET** handle, if a `CSocket` object is not attached to the handle, the member function returns **NULL** and does not create a temporary object.  
  
 For more information, see [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CSocket Class](../vs140/CSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::FromHandle](../vs140/CAsyncSocket--FromHandle.md)