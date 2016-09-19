---
title: "Indexers (C# Programming Guide)"
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
ms.assetid: 022cd27d-d5e0-4cfe-8b97-dc018cc3355d
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Indexers (C# Programming Guide)
Indexers allow instances of a class or struct to be indexed just like arrays. Indexers resemble [properties](../vs140/Properties--C#-Programming-Guide-.md) except that their accessors take parameters.  
  
 In the following example, a generic class is defined and provided with simple [get](../vs140/get--C#-Reference-.md) and [set](../vs140/set--C#-Reference-.md) accessor methods as a means of assigning and retrieving values. The `Program` class creates an instance of this class for storing strings.  
  
 [!CODE [csProgGuideIndexers#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideIndexers#9)]  
  
> [!NOTE]
>  For more examples, see [Related Sections](../vs140/Indexers--C#-Programming-Guide-.md#BKMK_RelatedSections).  
  
## Expression Body Definitions  
 It is common to have indexers that simply return immediately with the result of an expression.  There is a syntax shortcut for defining these indexers using `=>`:  
  
```c#  
public Customer this[long id] => store.LookupCustomer(id);  
```  
  
 The indexer must be read only, and you do not use the `get` accessor keyword.  
  
## Indexers Overview  
  
-   Indexers enable objects to be indexed in a similar manner to arrays.  
  
-   A `get` accessor returns a value. A `set` accessor assigns a value.  
  
-   The [this](../vs140/this--C#-Reference-.md) keyword is used to define the indexers.  
  
-   The [value](../vs140/value--C#-Reference-.md) keyword is used to define the value being assigned by the `set` indexer.  
  
-   Indexers do not have to be indexed by an integer value; it is up to you how to define the specific look-up mechanism.  
  
-   Indexers can be overloaded.  
  
-   Indexers can have more than one formal parameter, for example, when accessing a two-dimensional array.  
  
##  <a name="BKMK_RelatedSections"></a> Related Sections  
  
-   [Using Indexers](../Topic/Using%20Indexers%20\(C%23%20Programming%20Guide\).md)  
  
-   [Interface Indexers](../vs140/Indexers-in-Interfaces--C#-Programming-Guide-.md)  
  
-   [Comparison Between Properties and Indexers](../vs140/Comparison-Between-Properties-and-Indexers--C#-Programming-Guide-.md)  
  
-   [Asymmetric Accessor Accessibility (C# Programmer's Reference)](../vs140/Restricting-Accessor-Accessibility--C#-Programming-Guide-.md)  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Properties](../vs140/Properties--C#-Programming-Guide-.md)