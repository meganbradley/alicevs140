---
title: "IDebugFunctionObject2::Evaluate"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bc54c652-904b-4297-a6db-faa329684881
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugFunctionObject2::Evaluate
Calls the function and returns the resulting value as an object.  
  
## Syntax  
  
```cpp#  
HRESULT Evaluate (  
   IDebugObject** ppParams,  
   DWORD          dwParams,  
   DWORD          dwEvalFlags,  
   DWORD          dwTimeout,  
   IDebugObject** ppResult  
);  
```  
  
```c#  
int Evaluate (  
   IDebugObject     ppParams,  
   uint             dwParams,  
   uint             dwEvalFlags,  
   uint             dwTimeout,  
   out IDebugObject ppResult  
);  
```  
  
#### Parameters  
 `ppParams`  
 [in] An array of [IDebugObject](../vs140/IDebugObject.md) objects that represents the input parameters. Each of these parameters was created by using one of the Create methods in this interface.  
  
 `dwParams`  
 [in] The number of parameters in the `ppParams` array.  
  
 `dwEvalFlags`  
 [in] A combination of flags from the [EVALFLAGS](../vs140/EVALFLAGS.md) enumeration that specify how the evaluation is to be performed.  
  
 `dwTimeout`  
 [in] Specifies the maximum time, in milliseconds, to wait before returning from this method. Use **INFINITE** to wait indefinitely.  
  
 `ppResult`  
 [out] Returns an **IDebugObject** that represents the value of the function as an object.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugFunctionObject2](../vs140/IDebugFunctionObject2.md)