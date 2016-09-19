---
title: "Generic Interfaces (C# Programming Guide)"
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
ms.assetid: a8fa49a1-6e78-4a09-87e5-84a0b9f5ffbe
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Generic Interfaces (C# Programming Guide)
It is often useful to define interfaces either for generic collection classes, or for the generic classes that represent items in the collection. The preference for generic classes is to use generic interfaces, such as <xref:System.IComparable`1?qualifyHint=False> rather than <xref:System.IComparable?qualifyHint=False>, in order to avoid boxing and unboxing operations on value types. The .NET Framework class library defines several generic interfaces for use with the collection classes in the <xref:System.Collections.Generic?qualifyHint=False> namespace.  
  
 When an interface is specified as a constraint on a type parameter, only types that implement the interface can be used. The following code example shows a `SortedList<T>` class that derives from the `GenericList<T>` class. For more information, see [Generics Overview (C#)](../Topic/Introduction%20to%20Generics%20\(C%23%20Programming%20Guide\).md). `SortedList<T>` adds the constraint `where T : IComparable<T>`. This enables the `BubbleSort` method in `SortedList<T>` to use the generic <xref:System.IComparable`1.CompareTo?qualifyHint=False> method on list elements. In this example, list elements are a simple class, `Person`, that implements `IComparable<Person>`.  
  
 [!CODE [csProgGuideGenerics#29](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#29)]  
  
 Multiple interfaces can be specified as constraints on a single type, as follows:  
  
 [!CODE [csProgGuideGenerics#30](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#30)]  
  
 An interface can define more than one type parameter, as follows:  
  
 [!CODE [csProgGuideGenerics#31](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#31)]  
  
 The rules of inheritance that apply to classes also apply to interfaces:  
  
 [!CODE [csProgGuideGenerics#32](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#32)]  
  
 Generic interfaces can inherit from non-generic interfaces if the generic interface is contra-variant, which means it only uses its type parameter as a return value. In the .NET Framework class library, <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> inherits from <xref:System.Collections.IEnumerable?qualifyHint=False> because <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> only uses `T` in the return value of <xref:System.Collections.Generic.IEnumerable`1.GetEnumerator?qualifyHint=False> and in the <xref:System.Collections.Generic.IEnumerator`1.Current?qualifyHint=False> property getter.  
  
 Concrete classes can implement closed constructed interfaces, as follows:  
  
 [!CODE [csProgGuideGenerics#33](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#33)]  
  
 Generic classes can implement generic interfaces or closed constructed interfaces as long as the class parameter list supplies all arguments required by the interface, as follows:  
  
 [!CODE [csProgGuideGenerics#34](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#34)]  
  
 The rules that control method overloading are the same for methods within generic classes, generic structs, or generic interfaces. For more information, see [Generic Methods (C#)](../Topic/Generic%20Methods%20\(C%23%20Programming%20Guide\).md).  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Generics (C#)](../Topic/Introduction%20to%20Generics%20\(C%23%20Programming%20Guide\).md)   
 [interface](../vs140/interface--C#-Reference-.md)   
 [Generics in the .NET Framework](assetId:///2994d786-c5c7-4666-ab23-4c83129fe39c)