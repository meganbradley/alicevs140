---
title: "Compiler Error CS1519"
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
ms.topic: error-reference
ms.assetid: 186cef8e-c6c7-49aa-8b43-f6c2cb628414
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1519
Invalid token 'token' in class, struct, or interface member declaration  
  
 This error is generated whenever a token is encountered in a location where it does not belong. A *token* is a keyword; an identifier (the name of a class, struct, method, and so on); a string, character, or numeric literal value such as 108, "Hello", or 'A'; or an operator or punctuator such as `==` or `;`.  
  
 Any [class](../vs140/class--C#-Reference-.md), struct, or interface member declaration that contains invalid modifiers before the type will generate this error. To fix the error, remove the invalid modifiers.  
  
 The following sample generates CS1519 in five places because tokens are placed in locations where they are not valid:  
  
```c#  
// CS1519.cs  
// Generates CS1519 because a class name cannot be a number:  
class Test 42   
{  
// Generates CS1519 because of 'j' following 'I'  
// with no comma between them:  
    int i j;   
// Generates CS1519 because of "checked" on void method:  
    checked void f4();     
  
// Generates CS1519 because of "num":  
    void f5(int a num){}        
  
// Generates CS1519 because of namespace inside class:  
    namespace;             
  
}  
```  
  
## See Also  
 [Classes (C# Programming Guide)](../vs140/Classes--C#-Programming-Guide-.md)   
 [Structs (C# Programming Guide)](../vs140/Structs--C#-Programming-Guide-.md)   
 [Interfaces (C# Programming Guide)](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md)   
 [Methods (C# Programming Guide)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md)