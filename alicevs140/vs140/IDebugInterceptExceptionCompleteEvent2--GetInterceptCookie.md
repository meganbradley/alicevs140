---
title: "IDebugInterceptExceptionCompleteEvent2::GetInterceptCookie"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 07b20866-e598-4783-9ecc-6aa8625c8804
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugInterceptExceptionCompleteEvent2::GetInterceptCookie
Called when the processing of an intercepted exception has completed.  
  
## Syntax  
  
```cpp#  
HRESULT GetInterceptCookie(  
   UINT64* pqwCookie  
);  
```  
  
```c#  
int GetInterceptCookie(  
   out ulong pqwCookie  
);  
```  
  
#### Parameters  
 `pqwCookie`  
 [out] Unique value that is associated with the exception that was intercepted.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns error code.  
  
## Remarks  
 After the [IDebugStackFrame3::InterceptCurrentException](../vs140/IDebugStackFrame3--InterceptCurrentException.md) method has completed handling of an intercepted exception, it sends the [IDebugInterceptExceptionCompleteEvent2](../vs140/IDebugInterceptExceptionCompleteEvent2.md) event. The handler can use the `GetInterceptCookie` method to retrieve the unique value associated with the exception (the same value passed to the `InterceptCurrentException` method).  
  
## See Also  
 [IDebugStackFrame3::InterceptCurrentException](../vs140/IDebugStackFrame3--InterceptCurrentException.md)   
 [IDebugInterceptExceptionCompleteEvent2](../vs140/IDebugInterceptExceptionCompleteEvent2.md)