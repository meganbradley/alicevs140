---
title: "AfxSocketInit"
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
ms.assetid: a0ef181b-fd25-4866-ae9b-86cf06cb5ca5
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxSocketInit
Call this function in your `CWinApp::InitInstance` override to initialize Windows Sockets.  
  
## Syntax  
  
```  
  
      BOOL AfxSocketInit(  
   WSADATA* lpwsaData = NULL   
);  
```  
  
#### Parameters  
 `lpwsaData`  
 A pointer to a [WSADATA](../vs140/WSADATA-Structure.md) structure. If `lpwsaData` is not equal to `NULL`, then the address of the `WSADATA` structure is filled by the call to `WSAStartup`. This function also ensures that `WSACleanup` is called for you before the application terminates.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 When using MFC sockets in secondary threads in a statically linked MFC application, you must call `AfxSocketInit` in each thread that uses sockets to initialize the socket libraries. By default, `AfxSocketInit` is called only in the primary thread.  
  
## Code  
 [!CODE [NVC_MFCAsyncSocket#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAsyncSocket#4)]  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CWinApp::InitInstance](../vs140/CWinApp--InitInstance.md)