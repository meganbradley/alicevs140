---
title: "AfxThrowInternetException"
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
ms.topic: article
ms.assetid: c9645b10-9541-48b2-8b0c-94ca33fed3cb
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxThrowInternetException
Throws an Internet exception.  
  
## Syntax  
  
```  
  
      void AFXAPI AfxThrowInternetException(  
   DWORD dwContext,  
   DWORD dwError = 0   
);  
```  
  
#### Parameters  
 `dwContext`  
 The context identifier for the operation that caused the error. The default value of `dwContext` is specified originally in [CInternetSession](../vs140/CInternetSession-Class.md) and is passed to [CInternetConnection](../vs140/CInternetConnection-Class.md)- and [CInternetFile](../vs140/CInternetFile-Class.md)-derived classes. For specific operations performed on a connection or a file, you usually override the default with a `dwContext` of your own. This value then is returned to [CInternetSession::OnStatusCallback](../vs140/CInternetSession--OnStatusCallback.md) to identify the specific operation's status. For more information on context identifiers, see the article [Internet First Steps: WinInet](../vs140/WinInet-Basics.md).  
  
 `dwError`  
 The error that caused the exception.  
  
## Remarks  
 You are responsible for determining the cause based on the operating-system error code.  
  
> [!NOTE]
>  To call this function, your project must include AFXINET.H.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CInternetException Class](../vs140/CInternetException-Class.md)   
 [THROW](../vs140/THROW--MFC-.md)