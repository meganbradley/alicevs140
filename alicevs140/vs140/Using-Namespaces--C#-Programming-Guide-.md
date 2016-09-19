---
title: "Using Namespaces (C# Programming Guide)"
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
ms.assetid: 1fe8bf39-addc-438a-bd9e-86410e32381d
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using Namespaces (C# Programming Guide)
Namespaces are heavily used within C# programs in two ways. Firstly, the .NET Framework classes use namespaces to organize its many classes. Secondly, declaring your own namespaces can help control the scope of class and method names in larger programming projects.  
  
## Accessing Namespaces  
 Most C# applications begin with a section of `using` directives. This section lists the namespaces that the application will be using frequently, and saves the programmer from specifying a fully qualified name every time that a method that is contained within is used.  
  
 For example, by including the line:  
  
 [!CODE [csProgGuide#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuide#1)]  
  
 At the start of a program, the programmer can use the code:  
  
 [!CODE [csProgGuide#31](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuide#31)]  
  
 Instead of:  
  
 [!CODE [csProgGuide#30](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuide#30)]  
  
## Namespace Aliases  
 The [using directive](../Topic/using%20Directive%20\(C%23%20Reference\).md) can also be used to create an alias for a [namespace](../vs140/namespace--C#-Reference-.md). For example, if you are using a previously written namespace that contains nested namespaces, you might want to declare an alias to provide a shorthand way of referencing one in particular, as in the following example:  
  
 [!CODE [csProgGuideNamespaces#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#7)]  
  
## Using Namespaces to control scope  
 The `namespace` keyword is used to declare a scope. The ability to create scopes within your project helps organize code and lets you create globally-unique types. In the following example, a class titled `SampleClass` is defined in two namespaces, one nested inside the other. The [. operator](../vs140/.-Operator--C#-Reference-.md) is used to differentiate which method gets called.  
  
 [!CODE [csProgGuideNamespaces#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#8)]  
  
## Fully Qualified Names  
 Namespaces and types have unique titles described by fully qualified names that indicate a logical hierarchy. For example, the statement `A.B` implies that `A` is the name of the namespace or type, and `B` is nested inside it.  
  
 In the following example, there are nested classes and namespaces. The fully qualified name is indicated as a comment following each entity.  
  
 [!CODE [csProgGuideNamespaces#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#9)]  
  
 In the previous code segment:  
  
-   The namespace `N1` is a member of the global namespace. Its fully qualified name is `N1`.  
  
-   The namespace `N2` is a member of `N1`. Its fully qualified name is `N1.N2`.  
  
-   The class `C1` is a member of `N1`. Its fully qualified name is `N1.C1`.  
  
-   The class name `C2` is used two times in this code. However, the fully qualified names are unique. The first instance of `C2` is declared inside `C1`; therefore, its fully qualified name is: `N1.C1.C2`. The second instance of `C2` is declared inside a namespace `N2`; therefore, its fully qualified name is `N1.N2.C2`.  
  
 Using the previous code segment, you can add a new class member, `C3`, to the namespace `N1.N2` as follows:  
  
 [!CODE [csProgGuideNamespaces#10](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#10)]  
  
 In general, use `::` to reference a namespace alias or `global::` to reference the global namespace and `.` to qualify types or members.  
  
 It is an error to use `::` with an alias that references a type instead of a namespace. For example:  
  
 [!CODE [csProgGuideNamespaces#11](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#11)]  
  
 [!CODE [csProgGuideNamespaces#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#12)]  
  
 Remember that the word `global` is not a predefined alias; therefore, `global.X` does not have any special meaning. It acquires a special meaning only when it is used with `::`.  
  
 Compiler warning CS0440 is generated if you define an alias named global because `global::` always references the global namespace and not an alias. For example, the following line generates the warning:  
  
 [!CODE [csProgGuideNamespaces#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#13)]  
  
 Using `::` with aliases is a good idea and protects against the unexpected introduction of additional types. For example, consider this example:  
  
 [!CODE [csProgGuideNamespaces#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#14)]  
  
 [!CODE [csProgGuideNamespaces#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#15)]  
  
 This works, but if a type named `Alias` were to subsequently be introduced, `Alias.` would bind to that type instead. Using `Alias::Exception` insures that `Alias` is treated as a namespace alias and not mistaken for a type.  
  
 See the topic [How to: Use the global Namespace Qualifier](../Topic/How%20to:%20Use%20the%20Global%20Namespace%20Alias%20\(C%23%20Programming%20Guide\).md) for more information regarding the `global` alias.  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Namespaces (C#)](../vs140/Namespaces--C#-Programming-Guide-.md)   
 [Namespace Keywords](../vs140/Namespace-Keywords--C#-Reference-.md)   
 [. Operator](../vs140/.-Operator--C#-Reference-.md)   
 [:: Operator](../vs140/---Operator--C#-Reference-.md)   
 [extern (C# Programmer's Reference)](../Topic/extern%20\(C%23%20Reference\).md)