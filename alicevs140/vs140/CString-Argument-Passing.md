---
title: "CString Argument Passing"
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
ms.assetid: a67bebff-edf1-4cf4-bbff-d1cc6a901099
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CString Argument Passing
This article explains how to pass [CString](../vs140/CStringT-Class.md) objects to functions and how to return `CString` objects from functions.  
  
##  <a name="_core_cstring_argument.2d.passing_conventions"></a> CString Argument-Passing Conventions  
 When you define a class interface, you must determine the argument-passing convention for your member functions. There are some standard rules for passing and returning `CString` objects. If you follow the rules described in [Strings as Function Inputs](#_core_strings_as_function_inputs) and [Strings as Function Outputs](#_core_strings_as_function_outputs), you will have efficient, correct code.  
  
##  <a name="_core_strings_as_function_inputs"></a> Strings as Function Inputs  
 The most efficient and secure way to use a `CString` object in called functions is to pass a `CString` object to the function. Despite the name, a `CString` object does not store a string internally as a C-style string that has a null terminator. Instead, a `CString` object keeps careful track of the number of characters it has. Having `CString` provide a `LPCTSTR` pointer to a null-terminated string is a small amount of work that can become significant if your code has to do it constantly. The result is temporary because any change to the `CString` contents invalidates old copies of the `LPCTSTR` pointer.  
  
 It does make sense in some cases to provide a C-style string. For example, there can be a situation where a called function is written in C and does not support objects. In this case, coerce the `CString` parameter to `LPCTSTR`, and the function will get a C-style null-terminated string. You can also go the other direction and create a `CString` object by using the `CString` constructor that accepts a C-style string parameter.  
  
 If the string contents are to be changed by a function, declare the parameter as a nonconstant `CString` reference (**CString&**).  
  
##  <a name="_core_strings_as_function_outputs"></a> Strings as Function Outputs  
 Typically you can return `CString` objects from functions because `CString` objects follow value semantics like primitive types. To return a read-only string, use a constant `CString` reference (**const CString&**). The following example illustrates the use of `CString` parameters and return types:  
  
 [!CODE [NVC_ATLMFC_Utilities#197](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#197)]  
  
 [!CODE [NVC_ATLMFC_Utilities#198](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#198)]  
  
## See Also  
 [Strings (ATL/MFC)](../vs140/Strings--ATL-MFC-.md)