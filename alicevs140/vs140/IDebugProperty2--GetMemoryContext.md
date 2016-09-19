---
title: "IDebugProperty2::GetMemoryContext"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 91793d25-790f-4881-a5c0-d0458e534514
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProperty2::GetMemoryContext
Gets the memory context of the property value.  
  
## Syntax  
  
```cpp#  
HRESULT GetMemoryContext (   
   IDebugMemoryContext2** ppMemory  
);  
```  
  
```c#  
int GetMemoryContext(  
   out IDebugMemoryContext2 ppMemory  
);  
```  
  
#### Parameters  
 `ppMemory`  
 [out] Returns the [IDebugMemoryContext2](../vs140/IDebugMemoryContext2.md) object that represents the memory associated with this property.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns error code. Returns `S_GETMEMORYCONTEXT_NO_MEMORY_CONTEXT` if there is no memory context to retrieve.  
  
## See Also  
 [IDebugProperty2](../vs140/IDebugProperty2.md)   
 [IDebugMemoryContext2](../vs140/IDebugMemoryContext2.md)