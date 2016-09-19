---
title: "IDebugEngine2::RemoveSetException"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bdd25097-0e9d-4218-b417-0497ea48d2e8
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngine2::RemoveSetException
Removes the specified exception so it is no longer handled by the debug engine.  
  
## Syntax  
  
```cpp#  
HRESULT RemoveSetException(   
   EXCEPTION_INFO* pException  
);  
```  
  
```c#  
int RemoveSetException(   
   EXCEPTION_INFO[] pException  
);  
```  
  
#### Parameters  
 `pException`  
 [in] An [EXCEPTION_INFO](../vs140/EXCEPTION_INFO.md) structure that describes the exception to be removed.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The exception being removed must have been previously set by an earlier call to the [SetException](../vs140/IDebugEngine2--SetException.md) method.  
  
 To remove all set exceptions at once, call the [IDebugEngine2::RemoveAllSetExceptions](../vs140/IDebugEngine2--RemoveAllSetExceptions.md) method.  
  
## See Also  
 [IDebugEngine2](../vs140/IDebugEngine2.md)   
 [EXCEPTION_INFO](../vs140/EXCEPTION_INFO.md)