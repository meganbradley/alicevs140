---
title: "AND_CATCH"
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
ms.assetid: dcbdc1c7-4cbf-44d4-84ec-c0b60d0626a1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AND_CATCH
Defines a block of code for catching additional exception types thrown in a preceding **TRY** block.  
  
## Syntax  
  
```  
  
AND_CATCH(  
exception_class  
,   
exception_object_pointer_name )  
```  
  
#### Parameters  
 *exception_class*  
 Specifies the exception type to test for. For a list of standard exception classes, see class [CException](../vs140/CException-Class.md).  
  
 *exception_object_pointer_name*  
 A name for an exception-object pointer that will be created by the macro. You can use the pointer name to access the exception object within the `AND_CATCH` block. This variable is declared for you.  
  
## Remarks  
 Use the **CATCH** macro to catch one exception type, then the `AND_CATCH` macro to catch each subsequent type. End the **TRY** block with an `END_CATCH` macro.  
  
 The exception-processing code can interrogate the exception object, if appropriate, to get more information about the specific cause of the exception. Call the `THROW_LAST` macro within the `AND_CATCH` block to shift processing to the next outer exception frame. `AND_CATCH` marks the end of the preceding **CATCH** or `AND_CATCH` block.  
  
> [!NOTE]
>  The `AND_CATCH` block is defined as a C++ scope (delineated by curly braces). If you declare variables in this scope, remember that they are accessible only within that scope. This also applies to the *exception_object_pointer_name* variable.  
  
## Example  
 See the example for [CATCH](../vs140/CATCH.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [TRY](../vs140/TRY.md)   
 [CATCH](../vs140/CATCH.md)   
 [END_CATCH](../vs140/END_CATCH.md)   
 [THROW](../vs140/THROW--MFC-.md)   
 [THROW_LAST](../vs140/THROW_LAST.md)   
 [AND_CATCH_ALL](../vs140/AND_CATCH_ALL.md)   
 [CException Class](../vs140/CException-Class.md)