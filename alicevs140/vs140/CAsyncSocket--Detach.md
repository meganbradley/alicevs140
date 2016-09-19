---
title: "CAsyncSocket::Detach"
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
ms.assetid: 3a7a7efe-f03e-4908-8c05-c238c2d43aa9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::Detach
Call this member function to detach the **SOCKET** handle in the `m_hSocket` data member from the `CAsyncSocket` object and set `m_hSocket` to **NULL**.  
  
## Syntax  
  
```  
  
SOCKET Detach( );  
```  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::Attach](../vs140/CAsyncSocket--Attach.md)