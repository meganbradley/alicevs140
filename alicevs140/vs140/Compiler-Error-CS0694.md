---
title: "Compiler Error CS0694"
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
ms.assetid: 048615e4-4599-4726-b5db-55322ccc936f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0694
Type parameter 'identifier' has the same name as the containing type, or method  
  
 You must use a different name for the type parameter since the type parameter's name cannot be identical to the type or method name that contains the type parameter.  
  
## Example  
 The following sample generates CS0694.  
  
```  
// CS0694.cs  
// compile with: /target:library  
class C<C> {}   // CS0694  
```  
  
## Example  
 In addition to the above case involving a generic class, this error may occur with a method:  
  
```  
// CS0694_2.cs  
// compile with: /target:library  
class A  
{  
   public void F<F>(F arg);   // CS0694  
}  
```