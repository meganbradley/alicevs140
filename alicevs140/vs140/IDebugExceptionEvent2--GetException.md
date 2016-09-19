---
title: "IDebugExceptionEvent2::GetException"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7c98f41d-322b-4e72-a514-cbd4823eb70d
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExceptionEvent2::GetException
Gets a detailed description of the exception that fired this event.  
  
## Syntax  
  
```cpp#  
HRESULT GetException(   
   EXCEPTION_INFO* pExceptionInfo  
);  
```  
  
```c#  
int GetException(   
   EXCEPTION_INFO[] pExceptionInfo  
);  
```  
  
#### Parameters  
 `pExceptionInfo`  
 [in, out] An [EXCEPTION_INFO](../vs140/EXCEPTION_INFO.md) structure that is filled in with the description of the exception.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 [C++ only] The caller is responsible for freeing any strings in the [EXCEPTION_INFO](../vs140/EXCEPTION_INFO.md) structure as well as releasing the [IDebugProgram2](../vs140/IDebugProgram2.md) object in the structure.  
  
## See Also  
 [IDebugExceptionEvent2](../vs140/IDebugExceptionEvent2.md)   
 [EXCEPTION_INFO](../vs140/EXCEPTION_INFO.md)   
 [IDebugEvent2](../vs140/IDebugEvent2.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)