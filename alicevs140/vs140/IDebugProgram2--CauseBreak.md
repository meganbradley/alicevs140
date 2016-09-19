---
title: "IDebugProgram2::CauseBreak"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 07d353fc-68ab-4297-a18f-3d3c7a80e121
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgram2::CauseBreak
Requests that the program stop execution the next time one of its threads attempts to run.  
  
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
 An [IDebugBreakEvent2](../vs140/IDebugBreakEvent2.md) event is sent when the program next attempts to run code after this method is called.  
  
 This method is asynchronous in that the method returns immediately without necessarily waiting for the program to stop.  
  
## See Also  
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [IDebugBreakEvent2](../vs140/IDebugBreakEvent2.md)