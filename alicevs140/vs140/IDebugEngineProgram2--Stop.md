---
title: "IDebugEngineProgram2::Stop"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6e1c3d56-fb67-4a5b-80f9-8ee5131972bf
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngineProgram2::Stop
Stops all threads running in this program.  
  
## Syntax  
  
```cpp#  
HRESULT Stop(   
   void   
);  
```  
  
```c#  
int Stop();  
```  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method is called when this program is being debugged in a multi-program environment. When a stopping event from some other program is received, this method is called on this program. The implementation of this method should be asynchronous; that is, not all threads should be required to be stopped before this method returns. The implementation of this method may be as simple as calling the [IDebugProgram2::CauseBreak](../vs140/IDebugProgram2--CauseBreak.md) method on this program.  
  
 No debug event is sent in response to this method.  
  
## See Also  
 [IDebugEngineProgram2](../vs140/IDebugEngineProgram2.md)   
 [IDebugProgram2::CauseBreak](../vs140/IDebugProgram2--CauseBreak.md)