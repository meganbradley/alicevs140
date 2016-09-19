---
title: "Compiler COM Support Classes"
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
ms.topic: language-reference
ms.assetid: 6d800d9b-b902-4033-9639-740a30b06f88
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler COM Support Classes
**Microsoft Specific**  
  
 Standard classes are used to support some of the COM types. The classes are defined in comdef.h and the header files generated from the type library.  
  
|Class|Purpose|  
|-----------|-------------|  
|[_bstr_t](../vs140/_bstr_t-Class.md)|Wraps the `BSTR` type to provide useful operators and methods.|  
|[_com_error](../vs140/_com_error-Class.md)|Defines the error object thrown by [_com_raise_error](../vs140/_com_raise_error.md) in most failures.|  
|[_com_ptr_t](../vs140/_com_ptr_t-Class.md)|Encapsulates COM interface pointers, and automates the required calls to `AddRef`, **Release**, and `QueryInterface`.|  
|[_variant_t](../vs140/_variant_t-Class.md)|Wraps the **VARIANT** type to provide useful operators and methods.|  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler COM Support](../vs140/Compiler-COM-Support.md)   
 [Compiler COM Global Functions](../vs140/Compiler-COM-Global-Functions.md)   
 [C++ Language Reference](../vs140/C---Language-Reference.md)