---
title: "IDebugProgramPublisher2::SetDebuggerPresent"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c88c3ff4-3632-4199-b5de-83c6d21bcf75
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramPublisher2::SetDebuggerPresent
Tells the program publisher that a debugger is present and running.  
  
## Syntax  
  
```cpp  
HRESULT SetDebuggerPresent(  
   BOOL fDebuggerPresent  
);  
```  
  
```c#  
int SetDebuggerPresent(  
   int fDebuggerPresent  
);  
```  
  
#### Parameters  
 `fDebuggerPresent`  
 [in] Non-zero (`TRUE`) if a debugger is present, zero (`FALSE`) if it is not.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The presence or absence of a debugger is reflected in the data returned from the [IDebugProgramProvider2::GetProviderProcessData](../vs140/IDebugProgramProvider2--GetProviderProcessData.md) method: the value returned there is set or cleared by a prior call to the `SetDebuggerPresent` method.  
  
## See Also  
 [IDebugProgramPublisher2](../vs140/IDebugProgramPublisher2.md)   
 [IDebugProgramProvider2::GetProviderProcessData](../vs140/IDebugProgramProvider2--GetProviderProcessData.md)