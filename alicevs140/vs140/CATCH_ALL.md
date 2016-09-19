---
title: "CATCH_ALL"
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
ms.assetid: 089bfaec-f65a-49f8-a15e-97908842d6a6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CATCH_ALL
Defines a block of code that catches all exception types thrown in the preceding **TRY** block.  
  
## Syntax  
  
```  
  
CATCH_ALL(  
exception_object_pointer_name )  
```  
  
#### Parameters  
 *exception_object_pointer_name*  
 Specifies a name for an exception-object pointer that will be created by the macro. You can use the pointer name to access the exception object within the `CATCH_ALL` block. This variable is declared for you.  
  
## Remarks  
 The exception-processing code can interrogate the exception object, if appropriate, to get more information about the specific cause of the exception. Invoke the `THROW_LAST` macro to shift processing to the next outer exception frame. If you use `CATCH_ALL`, end the **TRY** block with an `END_CATCH_ALL` macro.  
  
> [!NOTE]
>  The `CATCH_ALL` block is defined as a C++ scope delineated by braces. If you declare variables in this scope, they are accessible only within that scope.  
  
 For more information on exceptions, see the article [Exceptions](../vs140/Exception-Handling-in-MFC.md).  
  
## Example  
 See the example for [CFile::Abort](../vs140/CFile--Abort.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [TRY](../vs140/TRY.md)   
 [AND_CATCH_ALL](../vs140/AND_CATCH_ALL.md)   
 [END_CATCH](../vs140/END_CATCH.md)   
 [THROW](../vs140/THROW--MFC-.md)   
 [THROW_LAST](../vs140/THROW_LAST.md)   
 [CATCH](../vs140/CATCH.md)   
 [CException Class](../vs140/CException-Class.md)