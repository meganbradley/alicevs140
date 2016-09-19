---
title: "TRACE"
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
ms.assetid: 7b6f42d8-b55a-4bba-ab04-c46251778e6f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# TRACE
Sends the specified string to the debugger of the current application.  
  
## Syntax  
  
```  
  
      TRACE(  
      exp  
       )  
TRACE(DWORD category, UINT level, LPCSTR lpszFormat, ... )  
```  
  
## Remarks  
 See [ATLTRACE2](../vs140/ATLTRACE2.md) for a description of **TRACE**.  **TRACE** and `ATLTRACE2` have the same behavior.  
  
 In the debug version of MFC, this macro sends the specified string to the debugger of the current application. In a release build, this macro compiles to nothing (no code is generated at all).  
  
 For more information, see [Debugging MFC Applications](../vs140/MFC-Debugging-Techniques.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxDump](../vs140/AfxDump--MFC-.md)