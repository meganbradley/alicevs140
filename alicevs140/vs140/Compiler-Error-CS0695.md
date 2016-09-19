---
title: "Compiler Error CS0695"
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
ms.assetid: 05f6c8cf-6147-4ac7-84ea-e1f34f8ef9f7
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0695
'generic type' cannot implement both 'generic interface' and 'generic interface' because they may unify for some type parameter substitutions  
  
 This error occurs when a generic class implements more than one parameterization of the same generic interface, and there exists a type parameter substitution which would make the two interfaces identical. To avoid this error, implement only one of the interfaces, or change the type parameters to avoid the conflict.  
  
 The following sample generates CS0695:  
  
```  
// CS0695.cs  
// compile with: /target:library  
  
interface I<T>  
{  
}  
  
class G<T1, T2> : I<T1>, I<T2>  // CS0695  
{  
}  
```