---
title: "Private Constructors (C# Programming Guide)"
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
ms.assetid: 29eeaa7d-8d81-453c-94b9-0e2800172621
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Private Constructors (C# Programming Guide)
A private constructor is a special instance constructor. It is generally used in classes that contain static members only. If a class has one or more private constructors and no public constructors, other classes (except nested classes) cannot create instances of this class. For example:  
  
 [!CODE [csProgGuideObjects#11](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#11)]  
  
 The declaration of the empty constructor prevents the automatic generation of a default constructor. Note that if you do not use an access modifier with the constructor it will still be private by default. However, the [private](../vs140/private--C#-Reference-.md) modifier is usually used explicitly to make it clear that the class cannot be instantiated.  
  
 Private constructors are used to prevent creating instances of a class when there are no instance fields or methods, such as the <xref:System.Math?qualifyHint=False> class, or when a method is called to obtain an instance of a class. If all the methods in the class are static, consider making the complete class static. For more information see [Static Classes and Static Class Members](../Topic/Static%20Classes%20and%20Static%20Class%20Members%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following is an example of a class using a private constructor.  
  
 [!CODE [csProgGuideObjects#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#12)]  
  
 Notice that if you uncomment the following statement from the example, it will generate an error because the constructor is inaccessible because of its protection level:  
  
 [!CODE [csProgGuideObjects#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#13)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Objects, Classes, and Structs (Visual C#)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)   
 [Constructors](../vs140/Constructors--C#-Programming-Guide-.md)   
 [Destructors (C# Programmer's Reference)](../Topic/Destructors%20\(C%23%20Programming%20Guide\).md)   
 [private (C# Programmer's Reference)](../vs140/private--C#-Reference-.md)   
 [public (C# Reference)](../vs140/public--C#-Reference-.md)