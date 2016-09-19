---
title: "CSocket::IsBlocking"
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
ms.assetid: dbe3bac9-7485-4852-9557-ec945d8be486
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSocket::IsBlocking
Call this member function to determine if a blocking call is in progress.  
  
## Syntax  
  
```  
  
BOOL IsBlocking( );  
```  
  
## Return Value  
 Nonzero if the socket is blocking; otherwise 0.  
  
## Remarks  
 For more information, see [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CSocket Class](../vs140/CSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSocket::CancelBlockingCall](../vs140/CSocket--CancelBlockingCall.md)