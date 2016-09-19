---
title: "Compiler Error CS0699"
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
ms.assetid: 1dff310b-6b8d-46b4-a649-bbf23282ff1f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0699
'generic' does not define type parameter 'identifier'  
  
 A type parameter was used in a generic definition that was not found in the declaration list of the type parameters for that generic. This can happen if the name used for the type parameter was inconsistent.  
  
 The following sample generates CS0699:  
  
```  
// CS0699.cs  
class C<T> where U : I   // CS0699 – U is not a valid type parameter  
{  
}  
```