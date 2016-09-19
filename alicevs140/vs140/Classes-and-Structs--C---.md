---
title: "Classes and Structs (C++)"
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
ms.assetid: 516dd496-13fb-4f17-845a-e9ca45437873
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Classes and Structs (C++)
This section introduces C++ classes and structs. The two constructs are identical in C++ except that in structs the default accessibility is public, whereas in classes the default is private.  
  
 Classes and structs are the constructs whereby you define your own types. Classes and structs can both contain data members and member functions, which enable you to describe the type's state and behavior.  
  
 The following topics are included:  
  
-   [class (C++)](../vs140/class--C---.md)  
  
-   [struct (C++)](../vs140/struct--C---.md)  
  
-   [Class Member Overview](../vs140/Class-Member-Overview.md)  
  
-   [Member Access Control (C++)](../vs140/Member-Access-Control--C---.md)  
  
-   [Inheritance  (C++)](../vs140/Inheritance---C---.md)  
  
-   [Static Members (C++)](../vs140/Static-Members--C---.md)  
  
-   [User-Defined Type Conversions (C++)](../vs140/User-Defined-Type-Conversions--C---.md)  
  
-   [Mutable Data Members (C++)](../vs140/Mutable-Data-Members--C---.md)  
  
-   [Nested Class Declarations](../vs140/Nested-Class-Declarations.md)  
  
-   [Anonymous Class Types](../vs140/Anonymous-Class-Types.md)  
  
-   [Pointers to Members](../vs140/Pointers-to-Members.md)  
  
-   [this Pointer](../vs140/this-Pointer.md)  
  
-   [C++ Bit Fields](../vs140/C---Bit-Fields.md)  
  
 The three class types are structure, class, and union. They are declared using the [struct](../vs140/struct--C---.md), [class](../vs140/class--C---.md), and [union](../vs140/Unions.md) keywords (see [Defining Class Types](assetId:///e8c65425-0f3a-4dca-afc2-418c3b1e57da)). The following table shows the differences among the three class types.  
  
 For more information on unions, see [Unions](../vs140/Unions.md). For information on managed classes and structs, see [Classes and Structs](../vs140/Classes-and-Structs---C---Component-Extensions-.md).  
  
### Access Control and Constraints of Structures, Classes and Unions  
  
|Structures|Classes|Unions|  
|----------------|-------------|------------|  
|class key is `struct`|class key is **class**|class key is **union**|  
|Default access is public|Default access is private|Default access is public|  
|No usage constraints|No usage constraints|Use only one member at a time|  
  
## See Also  
 [C++ Language Reference](../vs140/C---Language-Reference.md)