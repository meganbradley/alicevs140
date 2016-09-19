---
title: "Benefits of Generics (C# Programming Guide)"
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
ms.assetid: 80f037cd-9ea7-48be-bfc1-219bfb2d4277
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Benefits of Generics (C# Programming Guide)
Generics provide the solution to a limitation in earlier versions of the common language runtime and the C# language in which generalization is accomplished by casting types to and from the universal base type <xref:System.Object?qualifyHint=False>. By creating a generic class, you can create a collection that is type-safe at compile-time.  
  
 The limitations of using non-generic collection classes can be demonstrated by writing a short program that uses the <xref:System.Collections.ArrayList?qualifyHint=False> collection class from the .NET Framework class library. <xref:System.Collections.ArrayList?qualifyHint=False> is a highly convenient collection class that can be used without modification to store any reference or value type.  
  
 [!CODE [csProgGuideGenerics#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#4)]  
  
 But this convenience comes at a cost. Any reference or value type that is added to an <xref:System.Collections.ArrayList?qualifyHint=False> is implicitly upcast to <xref:System.Object?qualifyHint=False>. If the items are value types, they must be boxed when they are added to the list, and unboxed when they are retrieved. Both the casting and the boxing and unboxing operations decrease performance; the effect of boxing and unboxing can be very significant in scenarios where you must iterate over large collections.  
  
 The other limitation is lack of compile-time type checking; because an <xref:System.Collections.ArrayList?qualifyHint=False> casts everything to <xref:System.Object?qualifyHint=False>, there is no way at compile-time to prevent client code from doing something such as this:  
  
 [!CODE [csProgGuideGenerics#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#5)]  
  
 Although perfectly acceptable and sometimes intentional if you are creating a heterogeneous collection, combining strings and `ints` in a single <xref:System.Collections.ArrayList?qualifyHint=False> is more likely to be a programming error, and this error will not be detected until runtime.  
  
 In versions 1.0 and 1.1 of the C# language, you could avoid the dangers of generalized code in the .NET Framework base class library collection classes only by writing your own type specific collections. Of course, because such a class is not reusable for more than one data type, you lose the benefits of generalization, and you have to rewrite the class for each type that will be stored.  
  
 What <xref:System.Collections.ArrayList?qualifyHint=False> and other similar classes really need is a way for client code to specify, on a per-instance basis, the particular data type that they intend to use. That would eliminate the need for the upcast to `T:System.Object` and would also make it possible for the compiler to do type checking. In other words, <xref:System.Collections.ArrayList?qualifyHint=False> needs a type parameter. That is exactly what generics provide. In the generic <xref:System.Collections.Generic.List`1?qualifyHint=False> collection, in the `N:System.Collections.Generic` namespace, the same operation of adding items to the collection resembles this:  
  
 [!CODE [csProgGuideGenerics#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#6)]  
  
 For client code, the only added syntax with <xref:System.Collections.Generic.List`1?qualifyHint=False> compared to <xref:System.Collections.ArrayList?qualifyHint=False> is the type argument in the declaration and instantiation. In return for this slightly more coding complexity, you can create a list that is not only safer than <xref:System.Collections.ArrayList?qualifyHint=False>, but also significantly faster, especially when the list items are value types.  
  
## See Also  
 <xref:System.Collections.Generic?qualifyHint=False>   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Generics Overview (C#)](../Topic/Introduction%20to%20Generics%20\(C%23%20Programming%20Guide\).md)   
 [Boxing and Unboxing (C# Programming Guide)](../Topic/Boxing%20and%20Unboxing%20\(C%23%20Programming%20Guide\).md)   
 [Collections Best Practices](http://go.microsoft.com/fwlink/?LinkId=112403)