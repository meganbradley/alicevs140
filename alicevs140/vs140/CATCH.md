---
title: "CATCH"
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
ms.assetid: 227ebbe1-25f8-40cc-9244-e22b0a8ff570
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CATCH
Defines a block of code that catches the first exception type thrown in the preceding **TRY** block.  
  
## Syntax  
  
```  
  
CATCH(  
exception_class  
,   
exception_object_pointer_name )  
```  
  
#### Parameters  
 *exception_class*  
 Specifies the exception type to test for. For a list of standard exception classes, see class [CException](../vs140/CException-Class.md).  
  
 *exception_object_pointer_name*  
 Specifies a name for an exception-object pointer that will be created by the macro. You can use the pointer name to access the exception object within the **CATCH** block. This variable is declared for you.  
  
## Remarks  
 The exception-processing code can interrogate the exception object, if appropriate, to get more information about the specific cause of the exception. Invoke the `THROW_LAST` macro to shift processing to the next outer exception frame. End the **TRY** block with an `END_CATCH` macro.  
  
 If *exception_class* is the class `CException`, then all exception types will be caught. You can use the [CObject::IsKindOf](../vs140/CObject--IsKindOf.md) member function to determine which specific exception was thrown. A better way to catch several kinds of exceptions is to use sequential `AND_CATCH` statements, each with a different exception type.  
  
 The exception object pointer is created by the macro. You do not need to declare it yourself.  
  
> [!NOTE]
>  The **CATCH** block is defined as a C++ scope delineated by braces. If you declare variables in this scope, they are accessible only within that scope. This also applies to *exception_object_pointer_name*.  
  
 For more information on exceptions and the **CATCH** macro, see the article [Exceptions](../vs140/Exception-Handling-in-MFC.md).  
  
## Example  
 [!CODE [NVC_MFCExceptions#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCExceptions#26)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [TRY](../vs140/TRY.md)   
 [AND_CATCH](../vs140/AND_CATCH.md)   
 [END_CATCH](../vs140/END_CATCH.md)   
 [THROW](../vs140/THROW--MFC-.md)   
 [THROW_LAST](../vs140/THROW_LAST.md)   
 [CATCH_ALL](../vs140/CATCH_ALL.md)   
 [CException Class](../vs140/CException-Class.md)