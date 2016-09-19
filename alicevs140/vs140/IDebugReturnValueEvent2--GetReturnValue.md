---
title: "IDebugReturnValueEvent2::GetReturnValue"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 86c50d5a-6df6-4798-818a-c587a8741f90
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugReturnValueEvent2::GetReturnValue
Gets the value returned on stepping out of or over a function.  
  
## Syntax  
  
```cpp#  
HRESULT GetReturnValue (   
   IDebugProperty2** ppReturnValue  
);  
```  
  
```c#  
int GetReturnValue (   
   out IDebugProperty2 ppReturnValue  
);  
```  
  
#### Parameters  
 `ppReturnValue`  
 [out] Returns an [IDebugProperty2](../vs140/IDebugProperty2.md) object that represents the value to be retrieved.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugReturnValueEvent2](../vs140/IDebugReturnValueEvent2.md)   
 [IDebugProperty2](../vs140/IDebugProperty2.md)