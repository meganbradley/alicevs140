---
title: "BP_LOCATION_CODE_STRING"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a4cd71c6-5052-45fe-907b-ebc6ca1df2e4
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# BP_LOCATION_CODE_STRING
Used for setting code breakpoints based on a string that the user can enter from the integrated development environment (IDE).  
  
## Syntax  
  
```cpp#  
typedef struct _BP_LOCATION_CODE_STRING {   
   BSTR bstrContext;  
   BSTR bstrCodeExpr;  
} BP_LOCATION_CODE_STRING;  
```  
  
## Members  
 `bstrContext`  
 The context of the breakpoint within the code, typically a method or function name as seen on a call stack.  
  
 `bstrCodeExpr`  
 The string that the user types in to describe the code breakpoint.  
  
## Remarks  
 This structure is a member of the [BP_LOCATION](../vs140/BP_LOCATION.md) structure as part of a union.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../vs140/Structures-and-Unions.md)   
 [BP_LOCATION](../vs140/BP_LOCATION.md)