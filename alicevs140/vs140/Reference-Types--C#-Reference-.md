---
title: "Reference Types (C# Reference)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 801cf030-6e2d-4a0d-9daf-1431b0c31f47
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Reference Types (C# Reference)
There are two kinds of types in C#: reference types and value types. Variables of reference types store references to their data (objects), while variables of value types directly contain their data. With reference types, two variables can reference the same object; therefore, operations on one variable can affect the object referenced by the other variable. With value types, each variable has its own copy of the data, and it is not possible for operations on one variable to affect the other (except in the case of ref and out parameter variables, see [](../vs140/ref--C#-Reference-.md "ref (C# Reference)") and [](../vs140/out-parameter-modifier--C#-Reference-.md "out parameter modifier (C# Reference)")).  
  
 The following keywords are used to declare reference types:  
  
-   [class](../vs140/class--C#-Reference-.md)  
  
-   [interface](../vs140/interface--C#-Reference-.md)  
  
-   [delegate](../vs140/delegate--C#-Reference-.md)  
  
 C# also provides the following built-in reference types:  
  
-   [dynamic](../vs140/dynamic--C#-Reference-.md)  
  
-   [object](../vs140/object--C#-Reference-.md)  
  
-   [string](../Topic/string%20\(C%23%20Reference\).md)  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Types](../vs140/Types--C#-Reference-.md)   
 [Value Types](../Topic/Value%20Types%20\(C%23%20Reference\).md)