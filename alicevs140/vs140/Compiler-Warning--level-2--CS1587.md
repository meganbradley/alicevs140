---
title: "Compiler Warning (level 2) CS1587"
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
ms.assetid: b27c2009-d485-43fd-a649-fbc15570d256
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS1587
XML comment is not placed on a valid language element  
  
 Recommended tags for documentation comments are not allowed on all language elements. For example, a tag is not allowed on a namespace. For more information on XML comments, see [Recommended Tags for Documentation Comments](../vs140/Recommended-Tags-for-Documentation-Comments--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS1587:  
  
```  
// CS1587.cs  
// compile with: /W:2 /doc:x.xml  
  
/// <summary>test</summary>   // CS1587, tag not allowed on namespace  
namespace MySpace  
{  
    class MyClass  
    {  
        public static void Main()  
        {  
        }  
    }  
}  
```