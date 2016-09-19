---
title: "How to: Initialize Objects by Using an Object Initializer (C# Programming Guide)"
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
ms.assetid: 4b75ebb2-2e29-43de-929c-d736a8f27ce6
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Initialize Objects by Using an Object Initializer (C# Programming Guide)
You can use object initializers to initialize type objects in a declarative manner without explicitly invoking a constructor for the type.  
  
 The following examples show how to use object initializers with named objects. The compiler processes object initializers by first accessing the default instance constructor and then processing the member initializations. Therefore, if the default constructor is declared as `private` in the class, object initializers that require public access will fail.  
  
 You must use an object initializer if you're defining an anonymous type. For more information, see [How To: Use Anonymous Types in a Query Expression (C# Programming Guide)](../vs140/How-to--Return-Subsets-of-Element-Properties-in-a-Query--C#-Programming-Guide-.md).  
  
## Example  
 The following example shows how to initialize a new `StudentName` type by using object initializers.  
  
 [!CODE [csProgGuideLINQ#35](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#35)]  
  
## Example  
 The following example shows how to initialize a collection of `StudentName` types by using a collection initializer. Note that a collection initializer is a series of comma-separated object initializers.  
  
 [!CODE [csProgGuideLINQ#36](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#36)]  
  
## Compiling the Code  
 To run this code, copy and paste the class into a Visual C# console application project that has been created in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. For more information, see [How To: Create a LINQ Project](../vs140/How-to--Create-a-LINQ-Project.md).  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Object and Collection Initializers (C# Programming Guide)](../Topic/Object%20and%20Collection%20Initializers%20\(C%23%20Programming%20Guide\).md)