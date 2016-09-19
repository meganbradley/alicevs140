---
title: "Indexers in Interfaces (C# Programming Guide)"
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
ms.assetid: e16b54bd-4a83-4f52-bd75-65819fca79e8
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Indexers in Interfaces (C# Programming Guide)
Indexers can be declared on an [interface (C# Reference)](../vs140/interface--C#-Reference-.md). Accessors of interface indexers differ from the accessors of [class](../vs140/class--C#-Reference-.md) indexers in the following ways:  
  
-   Interface accessors do not use modifiers.  
  
-   An interface accessor does not have a body.  
  
 Thus, the purpose of the accessor is to indicate whether the indexer is read-write, read-only, or write-only.  
  
 The following is an example of an interface indexer accessor:  
  
 [!CODE [csProgGuideIndexers#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideIndexers#3)]  
  
 The signature of an indexer must differ from the signatures of all other indexers declared in the same interface.  
  
## Example  
 The following example shows how to implement interface indexers.  
  
 [!CODE [csProgGuideIndexers#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideIndexers#4)]  
  
 In the preceding example, you could use the explicit interface member implementation by using the fully qualified name of the interface member. For example:  
  
```  
public string ISomeInterface.this   
{   
}   
```  
  
 However, the fully qualified name is only needed to avoid ambiguity when the class is implementing more than one interface with the same indexer signature. For example, if an `Employee` class is implementing two interfaces, `ICitizen` and `IEmployee`, and both interfaces have the same indexer signature, the explicit interface member implementation is necessary. That is, the following indexer declaration:  
  
```  
public string IEmployee.this   
{   
}   
```  
  
 implements the indexer on the `IEmployee` interface, while the following declaration:  
  
```  
public string ICitizen.this   
{   
}   
```  
  
 implements the indexer on the `ICitizen` interface.  
  
## See Also  
 [C# Programming](../vs140/C#-Programming-Guide.md)   
 [Indexers](../vs140/Indexers--C#-Programming-Guide-.md)   
 [Properties](../vs140/Properties--C#-Programming-Guide-.md)   
 [Interfaces (C# Programming Guide)](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md)