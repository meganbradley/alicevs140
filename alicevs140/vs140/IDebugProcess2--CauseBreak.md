---
title: "IDebugProcess2::CauseBreak"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: efda8865-2319-4d53-90bf-6d9d74cd5195
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcess2::CauseBreak
Requests that the next program that is running code in this process halt and send an [IDebugBreakEvent2](../vs140/IDebugBreakEvent2.md) event object.  
  
## Syntax  
  
```cpp#  
HRESULT CauseBreak(   
   void  
);  
```  
  
```c#  
int CauseBreak();  
```  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugProcess2](../vs140/IDebugProcess2.md)