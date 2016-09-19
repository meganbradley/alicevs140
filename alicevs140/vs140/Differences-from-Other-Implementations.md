---
title: "Differences from Other Implementations"
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
ms.assetid: 944fed1c-52a0-4096-b88a-4941259ba3d0
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Differences from Other Implementations
## Microsoft Specific  
 The following list shows some differences between Microsoft C++ and other compilers.  
  
-   The compiler cannot instantiate a template outside of the module in which it is defined. Visual C++ does not support the **export** keyword.  
  
-   Templates cannot be used with functions declared with **__declspec (dllimport)** or **__declspec (dllexport)**.  
  
-   All template arguments must be of an unambiguous type that exactly matches that of the template parameter list. For example:  
  
    ```  
    template< class T > T check( T );  
    template< class S > void watch( int (*)(S) );  
    watch( check );     //error  
    ```  
  
     The compiler should instantiate the `check` templated function in the form `int check( int )`, but the inference cannot be followed.  
  
-   When resolving names used in class templates or function templates, all names are treated as dependent names.  See [Name Resolution for Dependent Types](../vs140/Name-Resolution-for-Dependent-Types.md)  
  
-   In a class template, the template parameter can be redefined in the scope of the class definition.  See [Name Resolution for Locally Declared Names](../vs140/Name-Resolution-for-Locally-Declared-Names.md)  
  
## END Microsoft Specific  
  
## See Also  
 [Templates](../vs140/Templates--C---.md)