---
title: "Compiler Error CS1910"
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
ms.assetid: 0fef9727-e56f-451c-9255-ca4e5a26d7c6
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1910
Argument of type 'type' is not applicable for the DefaultValue attribute  
  
 For parameters whose type is object, the argument of the <xref:System.Runtime.InteropServices.DefaultParameterValueAttribute?qualifyHint=False> must be `null`, an integral type, a floating point, `bool`, `string`, `enum`, or `char`. The argument can not be of type <xref:System.Type?qualifyHint=False> or any array type.  
  
## Example  
 The following sample generates CS1910.  
  
```  
// CS1910.cs  
// compile with: /target:library  
using System.Runtime.InteropServices;  
  
public interface MyI  
{  
   void Test([DefaultParameterValue(typeof(object))] object o);   // CS1910  
}  
```