---
title: "Compiler Warning (level 1) CS1584"
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
ms.assetid: 56c8f9bf-4cce-4269-b573-d60e5b11f9ab
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1584
XML comment on 'member' has syntactically incorrect cref attribute 'invalid_syntax'  
  
 One of the parameters passed to a tag for documentation comments has invalid syntax. For more information, see [Recommended Tags for Documentation Comments (C# Programmer's Reference)](../vs140/Recommended-Tags-for-Documentation-Comments--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS1584.  
  
```  
// CS1584.cs  
// compile with: /W:1 /doc:CS1584.xml  
/// <remarks>Test class</remarks>  
public class Test  
{  
   /// <remarks>Called in <see cref="Test.Mai()n"/>.</remarks>   // CS1584  
   // try the following line instead  
   // /// <remarks>Called in <see cref="Test.Main()"/>.</remarks>  
   public static void Test2() {}  
  
   /// <remarks>Main method</remarks>  
   public static void Main() {}  
}  
```