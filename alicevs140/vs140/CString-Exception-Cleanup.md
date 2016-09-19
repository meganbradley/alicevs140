---
title: "CString Exception Cleanup"
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
ms.topic: reference
ms.assetid: 28b9ce70-be63-4a0d-92a8-44bbfbc95e83
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CString Exception Cleanup
In previous versions of MFC, it was important that you clean up [CString](../vs140/CStringT-Class.md) objects after use. With MFC version 3.0 and later, explicit cleanup is no longer necessary.  
  
 Under the C++ exception handling mechanism that MFC now uses, you do not have to worry about cleanup after an exception. For a description of how C++ "unwinds" the stack after an exception is caught, see [the try, catch, and throw statements](../vs140/try--throw--and-catch-Statements--C---.md). Even if you use the MFC **TRY**/**CATCH** macros instead of the C++ keywords **try** and **catch**, MFC uses the C++ exception mechanism underneath, so you still do not need to clean up explicitly.  
  
## See Also  
 [Strings (ATL/MFC)](../vs140/Strings--ATL-MFC-.md)   
 [Exception Handling](../vs140/Exception-Handling-in-MFC.md)