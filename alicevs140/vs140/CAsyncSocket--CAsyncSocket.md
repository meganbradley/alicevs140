---
title: "CAsyncSocket::CAsyncSocket"
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
ms.assetid: 9fee6af3-e9cc-47d6-ba7e-e1759a9c65d3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::CAsyncSocket
Constructs a blank socket object.  
  
## Syntax  
  
```  
  
CAsyncSocket( );  
```  
  
## Remarks  
 After constructing the object, you must call its **Create** member function to create the **SOCKET** data structure and bind its address. (On the server side of a Windows Sockets communication, when the listening socket creates a socket to use in the **Accept** call, you do not call **Create** for that socket.)  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::Create](../vs140/CAsyncSocket--Create.md)