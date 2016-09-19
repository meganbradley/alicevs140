---
title: "AFX_COMCTL32_IF_EXISTS2"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ed7dab14-fcce-4ca6-983d-196062104c60
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_COMCTL32_IF_EXISTS2
Determines whether the Common Controls library implements the specified API (this is the Unicode version of [AFX_COMCTL32_IF_EXISTS](../vs140/AFX_COMCTL32_IF_EXISTS.md)).  
  
## Syntax  
  
```  
AFX_COMCTL32_IF_EXISTS2(  
   proc  
);  
```  
  
#### Parameters  
 `proc`  
 Pointer to a null-terminated string containing the function name, or specifies the function's ordinal value. If this parameter is an ordinal value, it must be in the low-order word; the high-order word must be zero. This parameter must be in Unicode.  
  
## Remarks  
 Use this macro to determine whether the Common Controls library the function specified by `proc` (instead of calling [GetProcAddress](../vs140/GetProcAddress.md)). This macro is the Unicode version of `AFX_COMCTL32_IF_EXISTS`.  
  
## Requirements  
 afxcomctl32.h, afxcomctl32.inl  
  
## See Also  
 [Isolation of the MFC Common Controls Library](../vs140/Isolation-of-the-MFC-Common-Controls-Library.md)   
 [AFX_COMCTL32_IF_EXISTS](../vs140/AFX_COMCTL32_IF_EXISTS.md)