---
title: "IDebugEngine2::SetException"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e6f5ec48-09e8-4b9b-9dc9-55f8d883f1b7
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngine2::SetException
Specifies how the debug engine (DE) should handle a given exception.  
  
## Syntax  
  
```cpp#  
HRESULT SetException(   
   EXCEPTION_INFO* pException  
);  
```  
  
```c#  
int SetException(   
   EXCEPTION_INFO[] pException  
);  
```  
  
#### Parameters  
 `pException`  
 [in] An [EXCEPTION_INFO](../vs140/EXCEPTION_INFO.md) structure that describes the exception and how to debug it.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 A DE could be instructed to stop the program generating an exception at first chance, second chance, or not at all.  
  
## See Also  
 [IDebugEngine2](../vs140/IDebugEngine2.md)   
 [EXCEPTION_INFO](../vs140/EXCEPTION_INFO.md)