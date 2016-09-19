---
title: "IDebugProcessEx2::Attach"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f3334ed7-39bf-4d02-a338-36f567b9b287
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcessEx2::Attach
This method informs the process that a session is now debugging the process.  
  
## Syntax  
  
```cpp#  
HRESULT Attach(   
   IDebugSession2* pSession  
);  
```  
  
```c#  
int Attach(  
   IDebugSession2 pSession  
);  
```  
  
#### Parameters  
 `pSession`  
 [in] A value that uniquely identifies the session attaching to this process.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The interface passed in `pSession` is to be treated only as a cookie, a value that uniquely identifies the session debug manager attaching to this process; none of the methods on the supplied interface are functional.  
  
## See Also  
 [IDebugProcessEx2](../vs140/IDebugProcessEx2.md)