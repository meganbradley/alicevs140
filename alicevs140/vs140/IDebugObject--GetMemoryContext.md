---
title: "IDebugObject::GetMemoryContext"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6760a0d3-a898-4e81-b68f-c45c584b225b
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugObject::GetMemoryContext
Gets the memory context that represents the address of the value of the object.  
  
## Syntax  
  
```cpp#  
HRESULT GetMemoryContext(   
   IDebugMemoryContext2** pContext  
);  
```  
  
```c#  
int GetMemoryContext(  
   ref IDebugMemoryContext2 pContext  
);  
```  
  
#### Parameters  
 `pContext`  
 [out] Returns an [IDebugMemoryContext2](../vs140/IDebugMemoryContext2.md) object representing the address of the value of the object.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 The returned memory context specifies the address of the value as represented by this [IDebugObject](../vs140/IDebugObject.md) object.  
  
## See Also  
 [IDebugMemoryContext2](../vs140/IDebugMemoryContext2.md)