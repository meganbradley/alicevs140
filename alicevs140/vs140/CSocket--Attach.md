---
title: "CSocket::Attach"
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
ms.assetid: f4671261-df05-412c-972e-9aeb3c213925
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSocket::Attach
Call this member function to attach the `hSocket` handle to a `CSocket` object.  
  
## Syntax  
  
```  
  
      BOOL Attach(  
   SOCKET hSocket   
);  
```  
  
#### Parameters  
 `hSocket`  
 Contains a handle to a socket.  
  
## Return Value  
 Nonzero if the function is successful.  
  
## Remarks  
 The **SOCKET** handle is stored in the object's [m_hSocket](../vs140/CAsyncSocket--m_hSocket.md) data member.  
  
 For more information, see [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
## Example  
 [!CODE [NVC_MFCSocketThread#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSocketThread#1)]  
  
 [!CODE [NVC_MFCSocketThread#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSocketThread#2)]  
  
 [!CODE [NVC_MFCSocketThread#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSocketThread#3)]  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CSocket Class](../vs140/CSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::Attach](../vs140/CAsyncSocket--Attach.md)