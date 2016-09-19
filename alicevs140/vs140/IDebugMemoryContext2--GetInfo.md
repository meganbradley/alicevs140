---
title: "IDebugMemoryContext2::GetInfo"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 08c7f091-1816-4d64-8834-f9ecaac5c58d
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugMemoryContext2::GetInfo
Retrieves a [CONTEXT_INFO](../vs140/CONTEXT_INFO.md) structure that describes the context.  
  
## Syntax  
  
```cpp#  
HRESULT GetInfo(   
   CONTEXT_INFO_FIELDS dwFields,  
   CONTEXT_INFO*       pInfo  
);  
```  
  
```c#  
int GetInfo(  
   enum_CONTEXT_INFO_FIELDS dwFields,   
   CONTEXT_INFO[]           pinfo  
);  
```  
  
#### Parameters  
 `dwFields`  
 [in] A combination of flags from the [CONTEXT_INFO_FIELDS](../vs140/CONTEXT_INFO_FIELDS.md) enumeration that indicate which fields of the [CONTEXT_INFO](../vs140/CONTEXT_INFO.md) structure are to be fill in.  
  
 `pInfo`  
 [in, out] The `CONTEXT_INFO` structure that is filled in.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugMemoryContext2](../vs140/IDebugMemoryContext2.md)   
 [CONTEXT_INFO_FIELDS](../vs140/CONTEXT_INFO_FIELDS.md)   
 [CONTEXT_INFO](../vs140/CONTEXT_INFO.md)