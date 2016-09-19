---
title: "exception_ptr"
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
ms.assetid: d39e329e-52d5-49be-8b4b-479e65833dc7
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# exception_ptr
A type that describes a pointer to an exception.  
  
## Syntax  
  
```cpp  
typedef unspecified exception_ptr;  
```  
  
## Remarks  
 An unspecified internal class that is used to implement the `exception_ptr` type.  
  
 Use an `exception_ptr` object to reference the current exception or an instance of a user-specified exception. In the Microsoft implementation, an exception is represented by an [EXCEPTION_RECORD](http://msdn.microsoft.com/library/windows/desktop/aa363082) structure. Each `exception_ptr` object includes an exception reference field that points to a copy of the `EXCEPTION_RECORD` structure that represents the exception.  
  
 When you declare an `exception_ptr` variable, the variable is not associated with any exception. That is, its exception reference field is NULL. Such an `exception_ptr` object is called a *null exception_ptr*.  
  
 Use the `current_exception` or `make_exception_ptr` function to assign an exception to an `exception_ptr` object. When you assign an exception to an `exception_ptr` variable, the variable's exception reference field points to a copy of the exception. If there is insufficient memory to copy the exception, the exception reference field points to a copy of a [std::bad_alloc](../vs140/bad_alloc-Class.md) exception. If the `current_exception` or `make_exception_ptr` function cannot copy the exception for any other reason, the function calls the [terminate (CRT)](../vs140/terminate--CRT-.md) function to exit the current process.  
  
 Despite its name, an `exception_ptr` object is not itself a pointer. It does not obey pointer semantics and cannot be used with the pointer member access (`->`) or indirection (*) operators. The `exception_ptr` object has no public data members or member functions.  
  
 **Comparisons:**  
  
 You can use the equal (`==`) and not-equal (`!=`) operators to compare two `exception_ptr` objects. The operators do not compare the binary value (bit pattern) of the `EXCEPTION_RECORD` structures that represent the exceptions. Instead, the operators compare the addresses in the exception reference field of the `exception_ptr` objects. Consequently, a null `exception_ptr` and the NULL value compare as equal.  
  
## See Also  
 [<exception\>](../vs140/-exception-.md)   
 [Transporting Exceptions Between Threads](../vs140/Transporting-Exceptions-Between-Threads.md)