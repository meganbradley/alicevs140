---
title: "How to: Know the Difference Between Passing a Struct and Passing a Class Reference to a Method (C# Programming Guide)"
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
ms.assetid: 9c1313a6-32a8-4ea7-a59f-450f66af628b
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Know the Difference Between Passing a Struct and Passing a Class Reference to a Method (C# Programming Guide)
The following example demonstrates how passing a [struct](../vs140/struct--C#-Reference-.md) to a method differs from passing a [class](../vs140/class--C#-Reference-.md) instance to a method. In the example, both of the arguments (struct and class instance) are passed by value, and both methods change the value of one field of the argument. However, the results of the two methods are not the same because what is passed when you pass a struct differs from what is passed when you pass an instance of a class.  
  
 Because a struct is a [value type](../Topic/Value%20Types%20\(C%23%20Reference\).md), when you [pass a struct by value](../vs140/Passing-Value-Type-Parameters--C#-Programming-Guide-.md) to a method, the method receives and operates on a copy of the struct argument. The method has no access to the original struct in the calling method and therefore can't change it in any way. The method can change only the copy.  
  
 A class instance is a [reference type](../vs140/Reference-Types--C#-Reference-.md), not a value type. When [a reference type is passed by value](../vs140/Passing-Reference-Type-Parameters--C#-Programming-Guide-.md) to a method, the method receives a copy of the reference to the class instance. That is, the method receives a copy of the address of the instance, not a copy of the instance itself. The class instance in the calling method has an address, the parameter in the called method has a copy of the address, and both addresses refer to the same object. Because the parameter contains only a copy of the address, the called method cannot change the address of the class instance in the calling method. However, the called method can use the address to access the class members that both the original address and the copy reference. If the called method changes a class member, the original class instance in the calling method also changes.  
  
 The output of the following example illustrates the difference. The value of the `willIChange` field of the class instance is changed by the call to method `ClassTaker` because the method uses the address in the parameter to find the specified field of the class instance. The `willIChange` field of the struct in the calling method is not changed by the call to method `StructTaker` because the value of the argument is a copy of the struct itself, not a copy of its address. `StructTaker` changes the copy, and the copy is lost when the call to `StructTaker` is completed.  
  
## Example  
 [!CODE [csProgGuideObjects#32](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#32)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Classes (C#)](../vs140/Classes--C#-Programming-Guide-.md)   
 [Structs (C#)](../vs140/Structs--C#-Programming-Guide-.md)   
 [Passing Parameters (C#)](../vs140/Passing-Parameters--C#-Programming-Guide-.md)