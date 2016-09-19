---
title: "Compiler Warning (level 1) CS1590"
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
ms.assetid: 0d6e5594-d6a6-43bf-8aa8-a452fa5748df
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1590
Invalid XML include element -- Missing file attribute  
  
 A path or doc attribute, passed to the [<include\>](../vs140/-include---C#-Programming-Guide-.md) tag, was missing or incomplete.  
  
 The following sample generates CS1590:  
  
```  
// CS1590.cs  
// compile with: /W:1 /doc:x.xml  
  
/// <include path='MyDocs/MyMembers[@name="test"]/*' />   // CS1590  
// try the following line instead  
// /// <include file='x.doc' path='MyDocs/MyMembers[@name="test"]/*' />  
class Test  
{  
   public static void Main()  
   {  
   }  
}  
```