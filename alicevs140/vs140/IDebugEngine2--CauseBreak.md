---
title: "IDebugEngine2::CauseBreak"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 17fe4698-b04e-4798-8412-80e0da60c387
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngine2::CauseBreak
Requests that all programs being debugged by this debug engine (DE) to stop execution the next time one of their threads attempts to run.  
  
## Syntax  
  
```cpp#  
HRESULT CauseBreak(   
   void   
);  
```  
  
```c#  
int CauseBreak();  
```  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method is asynchronous: an [IDebugBreakEvent2](../vs140/IDebugBreakEvent2.md) event is sent when the program next attempts to execute after this method is called.  
  
## See Also  
 [CauseBreak](../vs140/IDebugProgram2--CauseBreak.md)   
 [IDebugEngine2](../vs140/IDebugEngine2.md)