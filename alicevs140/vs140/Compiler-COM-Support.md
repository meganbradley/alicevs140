---
title: "Compiler COM Support"
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
ms.assetid: 76a78442-f2a4-4985-9967-67e20773f847
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler COM Support
## Microsoft Specific  
 The Visual C++ compiler can directly read component object model (COM) type libraries and translate the contents into C++ source code that can be included in the compilation. Language extensions are available to facilitate COM programming on the client side.  
  
 By using the [#import preprocessor directive](../vs140/#import-Directive--C---.md), the compiler can read a type library and convert it into a C++ header file that describes the COM interfaces as classes. A set of `#import` attributes is available for user control of the content for the resulting type library header files.  
  
 You can use the [__declspec](../vs140/__declspec.md) extended attribute [uuid](../vs140/uuid--C---.md) to assign a globally unique identifier (GUID) to a COM object. The keyword [__uuidof](../vs140/__uuidof-Operator.md) can be used to extract the GUID associated with a COM object. Another `__declspec` attribute, [property](../vs140/property--C---.md), can be used to specify the **get** and **set** methods for a data member of a COM object.  
  
 A set of COM support global functions and classes is provided to support the **VARIANT** and `BSTR` types, implement smart pointers, and encapsulate the error object thrown by `_com_raise_error`:  
  
-   [Compiler COM Global Functions](../vs140/Compiler-COM-Global-Functions.md)  
  
-   [_bstr_t](../vs140/_bstr_t-Class.md)  
  
-   [_com_error](../vs140/_com_error-Class.md)  
  
-   [_com_ptr_t](../vs140/_com_ptr_t-Class.md)  
  
-   [_variant_t](../vs140/_variant_t-Class.md)  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler COM Support Classes](../vs140/Compiler-COM-Support-Classes.md)   
 [Compiler COM Global Functions](../vs140/Compiler-COM-Global-Functions.md)