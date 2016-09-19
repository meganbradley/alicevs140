---
title: "&lt;new&gt;"
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
ms.assetid: 218e2a15-34e8-4ef3-9122-1e90eccf8559
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;new&gt;
Defines several types and functions that control the allocation and freeing of storage under program control. It also defines components for reporting on storage management errors.  
  
## Syntax  
  
```  
#include <new>  
  
```  
  
## Remarks  
 Some of the functions declared in this header are replaceable. The implementation supplies a default version, whose behavior is described in this document. A program can, however, define a function with the same signature to replace the default version at link time. The replacement version must satisfy the requirements described in this document.  
  
### Objects  
  
|||  
|-|-|  
|[nothrow](../vs140/-new--functions.md#nothrow)|Provides an object to be used as an argument for the `nothrow` versions of **new** and **delete**.|  
  
### Typedefs  
  
|||  
|-|-|  
|[new_handler](../vs140/-new--typedefs.md#new_handler)|A type that points to a function suitable for use as a new handler.|  
  
### Functions  
  
|||  
|-|-|  
|[set_new_handler](../vs140/-new--functions.md#set_new_handler)|Installs a user function that is called when new fails in its attempt to allocate memory.|  
  
### Operators  
  
|||  
|-|-|  
|[operator delete](../vs140/-new--operators.md#operator_delete)|The function called by a delete expression to deallocate storage for individual of objects.|  
|[operator delete&#91;&#93;](../vs140/-new--operators.md#operator_delete_at)|The function called by a delete expression to deallocate storage for an array of objects.|  
|[operator new](../vs140/-new--operators.md#operator_new)|The function called by a new expression to allocate storage for individual objects.|  
|[operator new&#91;&#93;](../vs140/-new--operators.md#operator_new_at)|The function called by a new expression to allocate storage for an array of objects.|  
  
### Classes  
  
|||  
|-|-|  
|[bad_alloc Class](../vs140/bad_alloc-Class.md)|The class describes an exception thrown to indicate that an allocation request did not succeed.|  
|[nothrow_t Class](../vs140/nothrow_t-Structure.md)|The class is used as a function parameter to operator new to indicate that the function should return a null pointer to report an allocation failure, rather than throw an exception.|  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)