---
title: "Partial Classes and Methods (C# Programming Guide)"
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
ms.assetid: 804cecb7-62db-4f97-a99f-60975bd59fa1
caps.latest.revision: 37
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Partial Classes and Methods (C# Programming Guide)
It is possible to split the definition of a [class](../vs140/class--C#-Reference-.md) or a [struct](../vs140/struct--C#-Reference-.md), an [interface](../vs140/interface--C#-Reference-.md) or a method over two or more source files. Each source file contains a section of the type or method definition, and all parts are combined when the application is compiled.  
  
## Partial Classes  
 There are several situations when splitting a class definition is desirable:  
  
-   When working on large projects, spreading a class over separate files enables multiple programmers to work on it at the same time.  
  
-   When working with automatically generated source, code can be added to the class without having to recreate the source file. Visual Studio uses this approach when it creates Windows Forms, Web service wrapper code, and so on. You can create code that uses these classes without having to modify the file created by Visual Studio.  
  
-   To split a class definition, use the [partial](../vs140/partial--Type---C#-Reference-.md) keyword modifier, as shown here:  
  
 [!CODE [csProgGuideObjects#26](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#26)]  
  
 The `partial` keyword indicates that other parts of the class, struct, or interface can be defined in the namespace. All the parts must use the `partial` keyword. All the parts must be available at compile time to form the final type. All the parts must have the same accessibility, such as `public`, `private`, and so on.  
  
 If any part is declared abstract, then the whole type is considered abstract. If any part is declared sealed, then the whole type is considered sealed. If any part declares a base type, then the whole type inherits that class.  
  
 All the parts that specify a base class must agree, but parts that omit a base class still inherit the base type. Parts can specify different base interfaces, and the final type implements all the interfaces listed by all the partial declarations. Any class, struct, or interface members declared in a partial definition are available to all the other parts. The final type is the combination of all the parts at compile time.  
  
> [!NOTE]
>  The `partial` modifier is not available on delegate or enumeration declarations.  
  
 The following example shows that nested types can be partial, even if the type they are nested within is not partial itself.  
  
 [!CODE [csProgGuideObjects#25](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#25)]  
  
 At compile time, attributes of partial-type definitions are merged. For example, consider the following declarations:  
  
 [!CODE [csProgGuideObjects#23](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#23)]  
  
 They are equivalent to the following declarations:  
  
 [!CODE [csProgGuideObjects#24](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#24)]  
  
 The following are merged from all the partial-type definitions:  
  
-   XML comments  
  
-   interfaces  
  
-   generic-type parameter attributes  
  
-   class attributes  
  
-   members  
  
 For example, consider the following declarations:  
  
 [!CODE [csProgGuideObjects#21](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#21)]  
  
 They are equivalent to the following declarations:  
  
 [!CODE [csProgGuideObjects#22](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#22)]  
  
### Restrictions  
 There are several rules to follow when you are working with partial class definitions:  
  
-   All partial-type definitions meant to be parts of the same type must be modified with `partial`. For example, the following class declarations generate an error:  
  
     [!CODE [csProgGuideObjects#20](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#20)]  
  
-   The `partial` modifier can only appear immediately before the keywords `class`, `struct`, or `interface`.  
  
-   Nested partial types are allowed in partial-type definitions as illustrated in the following example:  
  
     [!CODE [csProgGuideObjects#19](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#19)]  
  
-   All partial-type definitions meant to be parts of the same type must be defined in the same assembly and the same module (.exe or .dll file). Partial definitions cannot span multiple modules.  
  
-   The class name and generic-type parameters must match on all partial-type definitions. Generic types can be partial. Each partial declaration must use the same parameter names in the same order.  
  
-   The following keywords on a partial-type definition are optional, but if present on one partial-type definition, cannot conflict with the keywords specified on another partial definition for the same type:  
  
    -   [public](../vs140/public--C#-Reference-.md)  
  
    -   [private](../vs140/private--C#-Reference-.md)  
  
    -   [protected](../vs140/protected--C#-Reference-.md)  
  
    -   [internal](../vs140/internal--C#-Reference-.md)  
  
    -   [abstract](../vs140/abstract--C#-Reference-.md)  
  
    -   [sealed](../vs140/sealed--C#-Reference-.md)  
  
    -   base class  
  
    -   [new](../vs140/new--C#-Reference-.md) modifier (nested parts)  
  
    -   generic constraints  
  
         For more information, see [Constraints on Type Parameters (C# Programming Guide)](../Topic/Constraints%20on%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md).  
  
## Example 1  
  
### Description  
 In the following example, the fields and the constructor of the class, `CoOrds`, are declared in one partial class definition, and the member, `PrintCoOrds`, is declared in another partial class definition.  
  
### Code  
 [!CODE [csProgGuideObjects#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#17)]  
  
## Example 2  
  
### Description  
 The following example shows that you can also develop partial structs and interfaces.  
  
### Code  
 [!CODE [csProgGuideObjects#18](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#18)]  
  
## Partial Methods  
 A partial class or struct may contain a partial method. One part of the class contains the signature of the method. An optional implementation may be defined in the same part or another part. If the implementation is not supplied, then the method and all calls to the method are removed at compile time.  
  
 Partial methods enable the implementer of one part of a class to define a method, similar to an event. The implementer of the other part of the class can decide whether to implement the method or not. If the method is not implemented, then the compiler removes the method signature and all calls to the method. The calls to the method, including any results that would occur from evaluation of arguments in the calls, have no effect at run time. Therefore, any code in the partial class can freely use a partial method, even if the implementation is not supplied. No compile-time or run-time errors will result if the method is called but not implemented.  
  
 Partial methods are especially useful as a way to customize generated code. They allow for a method name and signature to be reserved, so that generated code can call the method but the developer can decide whether to implement the method. Much like partial classes, partial methods enable code created by a code generator and code created by a human developer to work together without run-time costs.  
  
 A partial method declaration consists of two parts: the definition, and the implementation. These may be in separate parts of a partial class, or in the same part. If there is no implementation declaration, then the compiler optimizes away both the defining declaration and all calls to the method.  
  
```  
// Definition in file1.cs  
partial void onNameChanged();  
  
// Implementation in file2.cs  
partial void onNameChanged()  
{  
  // method body  
}  
```  
  
-   Partial method declarations must begin with the contextual keyword [partial](../vs140/partial--Type---C#-Reference-.md) and the method must return [void](../vs140/void--C#-Reference-.md).  
  
-   Partial methods can have [ref](../vs140/ref--C#-Reference-.md) but not [out](../vs140/out--C#-Reference-.md) parameters.  
  
-   Partial methods are implicitly [private](../vs140/private--C#-Reference-.md), and therefore they cannot be [virtual](../vs140/virtual--C#-Reference-.md).  
  
-   Partial methods cannot be [extern](../Topic/extern%20\(C%23%20Reference\).md), because the presence of the body determines whether they are defining or implementing.  
  
-   Partial methods can have [static](../vs140/static--C#-Reference-.md) and [unsafe](../vs140/unsafe--C#-Reference-.md) modifiers.  
  
-   Partial methods can be generic. Constraints are put on the defining partial method declaration, and may optionally be repeated on the implementing one. Parameter and type parameter names do not have to be the same in the implementing declaration as in the defining one.  
  
-   You can make a [delegate](../vs140/delegate--C#-Reference-.md) to a partial method that has been defined and implemented, but not to a partial method that has only been defined.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Classes (C#)](../vs140/Classes--C#-Programming-Guide-.md)   
 [Structs (C#)](../vs140/Structs--C#-Programming-Guide-.md)   
 [Interfaces (Visual C#)](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md)   
 [partial (Type) (C# Reference)](../vs140/partial--Type---C#-Reference-.md)