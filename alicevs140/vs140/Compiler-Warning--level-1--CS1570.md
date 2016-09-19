---
title: "Compiler Warning (level 1) CS1570"
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
ms.assetid: a121d5c4-8b90-4cda-af5b-6ba8f23b2b1e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1570
XML comment on 'construct' has badly formed XML — 'reason'  
  
 When using [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md), any comments in the source code must be in XML. Any error with your XML markup will generate CS1570. For example:  
  
-   If you are passing a string to a **cref**, such as in an [<exception\>](../vs140/-exception---C#-Programming-Guide-.md) tag, the string must be enclosed in double quotation marks.  
  
-   If you are using a tag, such as [<seealso\>](../vs140/-seealso---C#-Programming-Guide-.md), which does not have a closing tag, you must specify a forward slash before the closing angle bracket.  
  
-   If you need to use a greater-than or less-than symbol in the text of description, you need to represent them with **&gt;** or **&lt;**.  
  
-   The file or path attribute on an [<include\>](../vs140/-include---C#-Programming-Guide-.md) tag was missing or improperly formed.  
  
 The following sample generates CS1570:  
  
```  
// CS1570.cs  
// compile with: /W:1  
namespace ns  
{  
   // the following line generates CS1570  
   /// <summary> returns true if < 5 </summary>  
   // try this instead  
   // /// <summary> returns true if <5 </summary>  
  
   public class MyClass  
   {  
      public static void Main ()  
      {  
      }  
   }  
}  
```