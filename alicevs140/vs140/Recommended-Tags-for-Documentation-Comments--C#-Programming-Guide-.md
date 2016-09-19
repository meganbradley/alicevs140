---
title: "Recommended Tags for Documentation Comments (C# Programming Guide)"
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
ms.assetid: 6e98f7a9-38f4-4d74-b644-1ff1b23320fd
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Recommended Tags for Documentation Comments (C# Programming Guide)
The C# compiler processes documentation comments in your code and formats them as XML in a file whose name you specify in the **/doc** command-line option. To create the final documentation based on the compiler-generated file, you can create a custom tool, or use a tool such as [Sandcastle](http://shfb.codeplex.com/).  
  
 Tags are processed on code constructs such as types and type members.  
  
> [!NOTE]
>  Documentation comments cannot be applied to a namespace.  
  
 The compiler will process any tag that is valid XML. The following tags provide generally used functionality in user documentation.  
  
## Tags  
  
||||  
|-|-|-|  
|[<c\>](../vs140/-c---C#-Programming-Guide-.md)|[<para\>](../vs140/-para---C#-Programming-Guide-.md)|[<see\>](../vs140/-see---C#-Programming-Guide-.md)*|  
|[<code\>](../vs140/-code---C#-Programming-Guide-.md)|[<param\>](../vs140/-param---C#-Programming-Guide-.md)*|[<seealso\>](../vs140/-seealso---C#-Programming-Guide-.md)*|  
|[<example\>](../vs140/-example---C#-Programming-Guide-.md)|[<paramref\>](../vs140/-paramref---C#-Programming-Guide-.md)|[<summary\>](../vs140/-summary---C#-Programming-Guide-.md)|  
|[<exception\>](../vs140/-exception---C#-Programming-Guide-.md)*|[<permission\>](../vs140/-permission---C#-Programming-Guide-.md)*|[<typeparam\>](../vs140/-typeparam---C#-Programming-Guide-.md)*|  
|[<include\>](../vs140/-include---C#-Programming-Guide-.md)*|[<remarks\>](../vs140/-remarks---C#-Programming-Guide-.md)|[<typeparamref\>](../vs140/-typeparamref---C#-Programming-Guide-.md)|  
|[<list\>](../vs140/-list---C#-Programming-Guide-.md)|[<returns\>](../vs140/-returns---C#-Programming-Guide-.md)|[<value\>](../vs140/-value---C#-Programming-Guide-.md)|  
  
 (* denotes that the compiler verifies syntax.)  
  
 If you want angle brackets to appear in the text of a documentation comment, use `<` and `>`, as shown in the following example.  
  
```xml  
/// <summary cref="C < T >">  
/// </summary>  
```  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [/doc (C# Compiler Options)](../Topic/-doc%20\(C%23%20Compiler%20Options\).md)   
 [XML Documentation Comments](../vs140/XML-Documentation-Comments--C#-Programming-Guide-.md)