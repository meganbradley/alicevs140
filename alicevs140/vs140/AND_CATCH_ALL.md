---
title: "AND_CATCH_ALL"
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
ms.assetid: ac983fa5-41cc-4fcf-8e9d-485398b04063
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AND_CATCH_ALL
Defines a block of code for catching additional exception types thrown in a preceding **TRY** block.  
  
## Syntax  
  
```  
  
AND_CATCH_ALL(  
exception_object_pointer_name )  
```  
  
#### Parameters  
 *exception_object_pointer_name*  
 A name for an exception-object pointer that will be created by the macro. You can use the pointer name to access the exception object within the `AND_CATCH_ALL` block. This variable is declared for you.  
  
## Remarks  
 Use the **CATCH** macro to catch one exception type, then the `AND_CATCH_ALL` macro to catch all other subsequent types. If you use `AND_CATCH_ALL`, end the **TRY** block with an `END_CATCH_ALL` macro.  
  
 The exception-processing code can interrogate the exception object, if appropriate, to get more information about the specific cause of the exception. Call the `THROW_LAST` macro within the `AND_CATCH_ALL` block to shift processing to the next outer exception frame. `AND_CATCH_ALL` marks the end of the preceding **CATCH** or `AND_CATCH_ALL` block.  
  
> [!NOTE]
>  The `AND_CATCH_ALL` block is defined as a C++ scope (delineated by braces). If you declare variables in this scope, remember that they are accessible only within that scope.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [TRY](../vs140/TRY.md)   
 [CATCH_ALL](../vs140/CATCH_ALL.md)   
 [END_CATCH_ALL](../vs140/END_CATCH_ALL.md)   
 [THROW](../vs140/THROW--MFC-.md)   
 [THROW_LAST](../vs140/THROW_LAST.md)   
 [AND_CATCH](../vs140/AND_CATCH.md)   
 [CException Class](../vs140/CException-Class.md)