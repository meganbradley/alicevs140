---
title: "IDiaStackFrame::get_systemExceptionHandling"
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
ms.assetid: c76cf265-dea0-4159-883f-32b50bbef044
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaStackFrame::get_systemExceptionHandling
Retrieves a flag that indicates whether system exception handling is in effect.  
  
## Syntax  
  
```cpp#  
HRESULT get_systemExceptionHandling (   
   BOOL* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns `TRUE` if system exception handling is in effect for this frame; otherwise, returns `FALSE`.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if the property is not supported. Otherwise, returns an error code.  
  
## Remarks  
 System exception handling is also known as structured exception handling. This is not the same thing as C++ exception handling.  
  
 To determine if C++ exception handling is in effect, call the [IDiaStackFrame::get_cplusplusExceptionHandling](../vs140/IDiaStackFrame--get_cplusplusExceptionHandling.md) method.  
  
## See Also  
 [IDiaStackFrame](../vs140/IDiaStackFrame.md)   
 [IDiaStackFrame::get_cplusplusExceptionHandling](../vs140/IDiaStackFrame--get_cplusplusExceptionHandling.md)