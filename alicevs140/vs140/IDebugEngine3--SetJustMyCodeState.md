---
title: "IDebugEngine3::SetJustMyCodeState"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8ec17fbf-df93-424a-b2ed-fd1e5ee51256
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngine3::SetJustMyCodeState
This method tells the debug engine about the JustMyCode state information.  
  
## Syntax  
  
```cpp  
HRESULT SetJustMyCodeState(  
   BOOL           fUpdate,  
   DWORD          dwModules,  
   JMC_CODE_SPEC* rgJMCSpec  
);  
```  
  
```c#  
int SetJustMyCodeState(  
   int             fUpdate,   
   uint            dwModules,   
   JMC_CODE_SPEC[] rgJMCSpec  
);  
```  
  
#### Parameters  
 `fUpdate`  
 [in] Nonzero (`TRUE`) to update current information, zero (`FALSE`) to reset all information (ignoring anything previously set).  
  
 `dwModules`  
 [in] Number of information structures in `rgJMCSpec.`  
  
 `rgJMCSpec`  
 [in] Array of [JMC_CODE_SPEC](../vs140/JMC_CODE_SPEC.md) structures to use.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns error code.  
  
## Remarks  
 JustMyCode is the concept of debugging only the code that belongs to a user and ignoring all intermediate code such as system code—even if source code is available for that system code.  
  
## See Also  
 [IDebugEngine3](../vs140/IDebugEngine3.md)   
 [JMC_CODE_SPEC](../vs140/JMC_CODE_SPEC.md)