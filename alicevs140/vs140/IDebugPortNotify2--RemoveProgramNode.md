---
title: "IDebugPortNotify2::RemoveProgramNode"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3668157b-66d2-416e-a359-fc04dcd18a48
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPortNotify2::RemoveProgramNode
Unregisters a program that can be debugged from the port it is running on.  
  
## Syntax  
  
```cpp#  
HRESULT RemoveProgramNode(   
   IDebugProgramNode2* pProgramNode  
);  
```  
  
```c#  
int RemoveProgramNode(   
   IDebugProgramNode2 pProgramNode  
);  
```  
  
#### Parameters  
 `pProgramNode`  
 [in] An [IDebugProgramNode2](../vs140/IDebugProgramNode2.md) objecy that represents the program to be unregistered.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method removes a program node that was added with a call to the [IDebugPortNotify2::AddProgramNode](../vs140/IDebugPortNotify2--AddProgramNode.md) method.  
  
## See Also  
 [IDebugPortNotify2](../vs140/IDebugPortNotify2.md)   
 [IDebugProgramNode2](../vs140/IDebugProgramNode2.md)   
 [IDebugPortNotify2::AddProgramNode](../vs140/IDebugPortNotify2--AddProgramNode.md)