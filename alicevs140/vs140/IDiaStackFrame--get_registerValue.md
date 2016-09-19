---
title: "IDiaStackFrame::get_registerValue"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cbe3d8ac-319a-40ac-bc3e-4eb81b2d7807
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaStackFrame::get_registerValue
Retrieves the value of a specified register as stored in the stack frame.  
  
## Syntax  
  
```cpp#  
HRESULT get_registerValue(  
   ULONG      registerIndex,  
   ULONGLONG *pRetVal  
);  
```  
  
#### Parameters  
 `registerIndex`  
 [in] One of the [CV_HREG_e](../vs140/CV_HREG_e.md) enumeration values.  
  
 `pRetVal`  
 [out] Value stored in the register.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns error code.  
  
## See Also  
 [IDiaStackFrame](../vs140/IDiaStackFrame.md)   
 [CV_HREG_e](../vs140/CV_HREG_e.md)