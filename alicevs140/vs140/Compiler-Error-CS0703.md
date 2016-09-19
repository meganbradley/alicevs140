---
title: "Compiler Error CS0703"
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
ms.topic: error-reference
ms.assetid: 3f488412-248e-40ad-9d76-96cb3eb73778
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0703
Inconsistent accessibility: constraint type 'identifier' is less accessible than 'identifier'  
  
 A constraint may not force the generic parameter to be less accessible than the generic class itself. In the following example, while the generic class C<T\> is declared public, the constraint attempts to force T to implement an internal interface. Even if this were allowed, only clients with internal access would be able to create the parameter for the class, so in effect, the class could be used only by clients with internal access.  
  
 To get rid of this error, make sure the access level of the generic class is not less restrictive than any classes or interfaces that appear in the bounds.  
  
 The following sample generates CS0703:  
  
```  
// CS0703.cs  
internal interface I {}  
public class C<T> where T : I  // CS0703 – I is internal; C<T> is public  
{  
}  
```