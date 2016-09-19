---
title: "CInternetException::m_dwContext"
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
ms.assetid: f4d62f9a-f620-4f58-932c-d9cbfea8de27
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetException::m_dwContext
The context value associated with the related Internet operation.  
  
## Syntax  
  
```  
  
DWORD_PTR m_dwContext;  
  
```  
  
## Remarks  
 The context identifier is originally specified in [CInternetSession](../vs140/CInternetSession-Class.md) and passed by MFC to [CInternetConnection](../vs140/CInternetConnection-Class.md)- and [CInternetFile](../vs140/CInternetFile-Class.md)-derived classes. You can override this default and assign any `dwContext` parameter a value of your choosing. `dwContext` is associated with any operation of the given object. `dwContext` identifies the operation's status information returned by [CInternetSession::OnStatusCallback](../vs140/CInternetSession--OnStatusCallback.md).  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetException Class](../vs140/CInternetException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CException Class](../vs140/CException-Class.md)