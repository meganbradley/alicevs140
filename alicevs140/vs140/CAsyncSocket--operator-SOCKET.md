---
title: "CAsyncSocket::operator SOCKET"
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
ms.assetid: 5b6253f4-f94f-48f4-a972-297eab3a22b4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::operator SOCKET
Use this operator to retrieve the **SOCKET** handle of the `CAsyncSocket` object.  
  
## Syntax  
  
```  
  
operator SOCKET( ) const;  
  
```  
  
## Return Value  
 If successful, the handle of the **SOCKET** object; otherwise, **NULL**.  
  
## Remarks  
 You can use the handle to call Windows APIs directly.  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)