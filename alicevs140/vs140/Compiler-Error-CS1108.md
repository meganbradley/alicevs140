---
title: "Compiler Error CS1108"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 26e82d6a-6ebf-4beb-912e-1bcb86b668aa
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1108
A parameter cannot have all the specified modifiers; there are too many modifiers on the parameter.  
  
 Certain combinations of parameter modifiers, such as `ref` and `out`, are not allowed because they have mutually exclusive meanings for the compiler.  
  
## Example  
 The following example generates CS1108:  
  
```  
// cs1108.cs  
// Compile with: /target:library  
public class Test  
{  
    // Regular Instance Method.  
        public void TestMethod(ref out int i) {} // CS1108  
  
}  
```