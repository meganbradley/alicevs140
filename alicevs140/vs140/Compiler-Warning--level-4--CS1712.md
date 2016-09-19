---
title: "Compiler Warning (level 4) CS1712"
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
ms.assetid: d9a8be26-c0ba-41fa-b082-1ce4ba7724b7
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) CS1712
Type parameter 'type parameter' has no matching typeparam tag in the XML comment on 'type' (but other type parameters do)  
  
 The documentation of a generic type is missing a **typeparam** tag. For more information, see [<typeparam\> (C# Programmer's Reference)](../vs140/-typeparam---C#-Programming-Guide-.md).  
  
## Example  
 The following code generates warning CS1712. To resolve this error, add a **typeparam** tag for the type parameter S.  
  
```  
// CS1712.cs  
// compile with: /doc:cs1712.xml  
using System;  
class Test  
{  
    public static void Main() {}  
    /// <param name="j"> This is the j parameter.</param>  
    /// <typeparam name="T"> This is the T type parameter.</typeparam>  
    public void bar<T,S>(int j) {}  // CS1712  
}  
```